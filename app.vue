<template>
  <Head>
    <Title>Creativepay</Title>
    <Link rel="icon" :href="icon" />
  </Head>

  <Navbar />
  <header id="hero" class="flex gap-8 mx-8 mt-10 flex-col justify-center items-center">
    <div class="header-tag">
      <p>
        <span>Creativepay 2023 release</span>
        <span class="circle"></span>
        <span>Job seeker</span>
      </p>
    </div>
    <p class="header-text">
      Empowering Creative Professionals to Find the Perfect Job
    </p>
    <p class="text-lg font-medium text-center opacity-50 text-[#1E1E1E] md:mx-52">
      We offer a user-friendly interface and advanced search filters that allow
      you to narrow down your search and find the right job faster.
    </p>
    <div class="flex justify-center py-8 px-14 gap-10 items-center border border-[#1E1E1E] rounded-3xl">
      <div>
        <p class="number">20.5+</p>
        <p>Million Users</p>
      </div>
      <div>
        <p class="number">7.8 B+</p>
        <p>Jobs Posted</p>
      </div>
      <div>
        <p class="number">201 M</p>
        <p>Proposals Sent</p>
      </div>
    </div>
    <button type="button" class="button">Get Started <img class="inline absolute h-5 mt-[3px] ml-1.5"
        src="~/assets/svg/btn_arrow.svg" alt="" />
    </button>
    <img src="~/assets/images/header-image.png" alt="image showing map" class="w-4/5 shadow-lg" />
  </header>

  <section id="discover" class="flex flex-col gap-8 justify-center mx-8 mt-32 items-center">
    <h1 class="header-tag">
      Discover Jobs
    </h1>
    <p class="header-text text-center">
      Explore a World of Job Opportunities and Find Your Perfect Fit
    </p>
    <div class="">
      <i class="text-center absolute w-6 mt-[5px] ml-5 "><img src="~/assets/svg/search.svg" class="inline"></i>
      <input type="search" name="search-bar" id="search-bar" placeholder="Search by company name or role..." disabled
        class="rounded-3xl w-[340px] pl-14 py-2 leading-tight bg-[#ECEDEB33] border border-[#A1C8CA]" />
    </div>
    <div class="flex flex-row flex-wrap justify-center gap-16">
      <div v-for="card in discover_cards" class="discover-card">
        <div class="discover-card-image">
          <img :src="card.src" alt="" class="" />
        </div>
        <div class="">
          <p class="my-5 discover-card-header">
            {{ card.title }}
            <img src="~/assets/svg/arrow.svg" alt="" class="inline">
          </p>
          <p class="discover-card-text">{{ card.description }}</p>
        </div>
      </div>
    </div>
    <button type="button" class="button">Browse more roles <img class="inline h-5 mt-[3px] ml-1 absolute"
        src="~/assets/svg/btn_arrow.svg" alt="" /></button>
  </section>

  <!-- <section id="for-candidate" class="flex flex-col gap-8 justify-center mx-8 mt-28 px-6 py-12 items-start">
    <h1 class="header-tag">
      For Candidate
    </h1>
    <p class="header-text">
      Create your profile for free and start now
    </p>
  </section> -->

  <section id="feature-advantage" class="flex flex-col gap-8 justify-center mx-8 mt-28 items-center">
    <h1 class="header-tag">
      Feature Advantage
    </h1>
    <p class="header-text">
      Keep in touch with recruiters with our easy made tool
    </p>
    <img src="~/assets/images/table_container.png" alt="">
  </section>

  <!-- <section id="today-job" class="flex flex-col gap-8 justify-center mx-8 mt-28 px-6 py-12 items-start">
    <h1 class="header-tag">
      Today's Job
    </h1>
    <p class="header-text text-left">
      Check today's job opportunities
    </p>
    <div class="flex flex-row justify-start">
      <div class="job-card">
        <div class="job-card-image">
          <img src="" alt="">
        </div>
        <div class="job-card-header">
          BQ LTD
        </div>
        <div class="job-card-text">
          A company specializing in underwater exploration and research. They develop and use advanced technology y to
          discover new species, study marine life, and find solutions to protect and conserve the ocean.
        </div>
        <div>
          <span class="job-card-tag bg-[#6260dd26] text-[#6260DD]">3D Illustration</span>
          <span class="job-card-tag bg-[#1C1F3226] text-[#1C1F32]">Product Design</span>
        </div>
      </div>
    </div>
  </section> -->

  <!-- <section>
    <h1 class="header-tag">
      Our podcast
    </h1>
    <p class="header-text">
      Hear what we have to say about our openings
    </p>
  </section> -->

  <footer
    class="grid grid-flow-row grid-cols-4 md:grid-cols-[6fr_1fr_1fr_1fr_1fr] py-14 px-10 gap-x-10 mt-28 bg-[#FAFBFA]">
    <div>
      <img src="~/assets/images/icon.png" class="inline absolute mt-0.5 w-8" alt="">
      <p class="inline ml-10 text-2xl">Creativepay</p>
    </div>
    <div>
      <p class="footer-header">Creativepay</p>
      <ul>
        <li>Job</li>
        <li>Companies</li>
        <li>Features</li>
        <li>Pricing</li>
        <li>Changelog</li>
      </ul>
    </div>
    <div>
      <p class="footer-header">Social Media</p>
      <ul>
        <a href="#">
          <li>Facebook</li>
        </a>
        <a href="#">
          <li>Instagram</li>
        </a>
        <a href="#">
          <li>Twitter</li>
        </a>
        <a href="#">
          <li>Tiktok</li>
        </a>
      </ul>
    </div>
    <div>
      <p class="footer-header">Help</p>
      <ul>
        <li>FAQs</li>
        <li>Support</li>
      </ul>
    </div>
    <div>
      <p class="footer-header">Contact</p>
      <ul>
        <li>+234 916 161 8102</li>
        <li>hellocreativepay.com</li>
      </ul>
    </div>
  </footer>
</template>

<script>
import icon from "~/assets/icon/Icon.ico"

import imgUI from "~/assets/images/ui_designer.png"
import imgVisual from "~/assets/images/visual_animator.png"
import imgArt from "~/assets/images/art_director.png"
import imgFont from "~/assets/images/font_designer.png"
import imgFront from "~/assets/images/front_dev.png"
import imgBack from "~/assets/images/back_dev.png"
import imgUX from "~/assets/images/ux_research.png"
import img3D from "~/assets/images/3d_designer.png"
import imgGraphics from "~/assets/images/graphics_designer.png"



export default {
  data() {
    return {
      icon,
      discover_cards: [
        {
          title: "UI Designer",
          description: "Designing the visual elements of a digital product or website. They create the overall look and feel of the interface, including the layout, typography, color scheme, and graphical elements such as buttons and icons.",
          src: imgUI,
        },
        {
          title: "Visual Animator",
          description: "Creates animations and visual effects for various forms of media, such as films, video games, television shows, and advertisements. They use a combination of traditional and digital animation techniques to bring characters, objects, and environments to life",
          src: imgVisual,
        },
        {
          title: "Art Director",
          description: "visual style and creative direction of a project, such as an advertising campaign, magazine layout, film, or video game. Art directors are typically employed in the fields of advertising, graphic design, or the entertainment industry.",
          src: imgArt,
        },
        {
          title: "Font Designer",
          description: "A font designer, also known as a type designer, is a professional who creates fonts or typefaces. Fonts are a critical component of graphic design, as they impact the readability, legibility, and overall visual appeal of text in print and digital media.",
          src: imgFont,
        },
        {
          title: "Front End Developer",
          description: "specializes in designing and developing the user interface and user experience of websites, web applications, and other digital products. They work closely with designers and back-end developers",
          src: imgFront,
        },
        {
          title: "Back End Developer",
          description: "specializes in designing and developing the server-side components of web applications and other digital products. They work closely with front-end developers to ensure that the user ",
          src: imgBack,
        },
        {
          title: "UX Researcher",
          description: "specializes in conducting user experience research to inform the design and development of products, websites, and other digital experiences. They work closely with designers, developers, and other ",
          src: imgUX,
        },
        {
          title: "3D Designer",
          description: "specializes in creating 3D digital models of objects and environments using specialized software. They work in various industries, including film and television, video games, architecture, product design, and advertising.",
          src: img3D,
        },
        {
          title: "Graphics Designer",
          description: "specializes in creating visual content to communicate a message or idea through various mediums such as print, digital media, and branding. They work in various industries, including advertising, marketing, publishing, and entertainment.",
          src: imgGraphics,
        },
      ]
    }
  }
}
</script>

<style scoped>
/* @import url("~/assets/css/index.css"); */

p {
  letter-spacing: -0.7px;
}

@media screen and (max-width: 768px) {
  footer>div:first-child {
    display: none;
  }

  .discover-card {
    width: 40% !important;
  }
}

@media screen and (min-width: 768px) {}

li {
  list-style-type: none;
}

.footer-header {
  font-weight: 700;
  letter-spacing: -0.3px;
  font-size: 18px;
  color: #1C1F32;
  margin-bottom: 12px;
}

footer li {
  margin-bottom: 10px;
  color: #1E1E1ECC;
  font-size: 16px;
  font-weight: 600;
}

#hero>div:first-child {
  letter-spacing: -0.05em;
}

#hero>p:first-child {
  background: linear-gradient(93.66deg,
      #1c1f32 -1.44%,
      #1c1f32 -1.43%,
      #6260dd 76.08%);
}

#hero .number {
  color: #43437A;
  font-size: 40px;
  font-weight: 600;
  text-align: center;
}

#hero .number+p {
  color: #1E1E1E;
  opacity: 0.5;
  font-weight: 500;
  text-align: center;
  font-size: 26px;
}

.button {
  color: #ECEDEB;
  padding: 0.5rem 2.4rem 0.5rem 1rem;
  border-radius: 25px;
  font-weight: 600;
  font-size: 16px;
  background: #6260DD;
}

.header-tag {
  padding: 4px 20px;
  background: rgba(241, 241, 253, 1);
  border-radius: 20px;
  font-weight: 600;
  font-size: 14px;
  color: rgba(30, 30, 30, 0.5);
  text-align: center;
}

.header-tag .circle {
  background: #1E1E1E80;
  display: inline-block;
  width: 10px;
  height: 10px;
  border-radius: 50%;
  margin: 0px 10px;
}

.header-text {
  /* text-5xl font-bold border md:mx-52 text-center leading-tight  */
  font-size: 3rem;
  font-weight: bold;
  text-align: center;
  color: #1C1F32;
  background-color: white;
  background-image: linear-gradient(93.66deg, #1C1F32 -1.44%, #1C1F32 -1.43%, #6260DD 76.08%);
  -webkit-text-fill-color: transparent;
  background-clip: text;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  margin: 0px 3rem;
}

.discover-card {
  /* border p-5 w-1/3 md:w-1/4  */
  padding: 1.5rem 1.25rem;
  width: 25%;
  background: white;
}

.discover-card:hover {
  outline: 2px solid rgba(67, 67, 122, 1);
  border-radius: 20px;
}

.discover-card-image {
  width: 50px;
  border-radius: 5px;
  box-shadow: 0 1px 2px 0 rgb(0 0 0 / 0.05);
}

.discover-card-image img {
  margin: auto;
  width: 40px;
}

.discover-card-header {
  color: rgba(67, 67, 122, 1);
  font-weight: 600;
}

.discover-card-text {
  font-size: 14px;
  opacity: 0.5;
  font-weight: 600;
  color: #1e1e1e;
}

#for-candidate,
#today-job {
  background: rgba(236, 237, 235, 1);
}

.job-card {
  background: white;
  padding: 18px 16px;
}

.job-card-image {}

.job-card-header {
  color: rgba(30, 30, 30, 0.8);
  font-weight: 700;
  font-size: 20px;
}

.job-card-text {
  color: rgba(30, 30, 30, 0.8);
  font-weight: 600;
  font-size: 16px;
}

.job-card-tag {
  padding: 8px 14-+px;
  margin-right: 10px;
  border-radius: 20px;
  font-weight: 600;
  font-size: 11px;
}
</style>
