<template>
  <div class="body">

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
      <p class="text-lg font-bold text-center opacity-50 text-[#1E1E1E] md:mx-28 lg:mx-52">
        We offer a user-friendly interface and advanced search filters that allow
        you to narrow down your search and find the right job faster.
      </p>
      <div
        class="number-box flex flex-col sm:flex-row justify-center py-8 px-10 gap-10 items-center border border-[#1E1E1E] rounded-3xl">
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
      <img src="~/assets/images/header-image.png" alt="image showing map" class="w-11/12 md:w-4/5 shadow-lg" />
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
      <div class="flex flex-row flex-wrap justify-around gap-4 gap-y-8">
        <div v-for="card in discover_cards" class="discover-card w-4/5 md:w-5/12 xl:w-1/4">
          <div class="discover-card-image">
            <img :src="card.src" alt="" class="" />
          </div>
          <div class="">
            <p class="my-3 discover-card-header">
              {{ card.title }}
              <img src="~/assets/svg/arrow.svg" alt="" class="inline pl-2">
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
      <img src="~/assets/images/table_container.png" alt="" class="w-11/12">
    </section>

    <section id="today-job"
      class="flex flex-col gap-8 justify-center items-start mx-8 lg:mx-20 mt-28 px-8 lg:px-16 py-12">
      <h1 class="header-tag">
        Today's Job
      </h1>
      <div class="flex flex-row flex-wrap justify-between items-center gap-10 w-full lg:pr-10">
        <p class="header-text">
          Check today's job opportunities
        </p>
        <button type="button" class="button">Previous featured jobs <img class="inline h-5 mt-[3px] ml-1 absolute"
            src="~/assets/svg/btn_arrow.svg" alt="" /></button>
      </div>
      <div class="flex flex-row flex-wrap justify-center lg:justify-between items-center gap-y-8 gap-x-8 mt-4">
        <div v-for="card in job_cards" class="job-card px-8 py-10 rounded-md w-4/5 md:w-5/12 xl:w-1/4">
          <div class="job-card-image mb-6">
            <img :src="card.src" :alt="card.title + ' logo'">
          </div>
          <div class="job-card-header font-bold text-xl mb-3">
            {{ card.title }}
          </div>
          <div class="job-card-text font-semibold text-base mb-3">
            {{ card.description }}
          </div>
          <div>
            <span v-for="tag in card.tags" class="job-card-tag" :class="`bg-[${tag.bgColor}] text-[${tag.color}]`">
              {{ tag.title }}
            </span>
          </div>
        </div>
      </div>
    </section>

    <!-- <section>
    <h1 class="header-tag">
      Our podcast
    </h1>
    <p class="header-text">
      Hear what we have to say about our openings
    </p>
  </section> -->

    <footer class="flex flex-col lg:flex-row lg:px-24 gap-4 lg:gap-12 justify-between py-14 px-10 mt-28 bg-[#FAFBFA]">
      <div class="mb-10">
        <img src="~/assets/images/icon.png" class="inline absolute mt-0.5 w-8" alt="">
        <p class="inline ml-10 text-2xl">Creativepay</p>
      </div>
      <div class="grid grid-flow-row grid-cols-2 md:grid-cols-4 gap-8">
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
      </div>
    </footer>
  </div>
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

import imgBQ from "~/assets/images/bq_ltd.png"
import imgBeyond from "~/assets/images/beyond.png"
import imgEcho from "~/assets/images/echo_dyn.png"
import imgNeo from "~/assets/images/neo_health.png"
import imgSolaris from "~/assets/images/solaris.png"
import imgTimeKeep from "~/assets/images/time_keep.png"

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
      ],
      job_cards: [
        {
          title: "BQ LTD",
          description: "A company specializing in underwater exploration and research. They develop and use advanced technology to discover new species, study marine life, and find solutions to protect and conserve the ocean.",
          src: imgBQ,
          tags: [{ title: "3D Illustration", bgColor: "#6260dd26", color: "#6260DD" }, { title: "Product Design", bgColor: "#1C1F3226", color: "#1C1F32" }]
        },
        {
          title: "Solaris Energy",
          description: "Solaris Energy is a renewable energy company that specializes in solar technology. They develop and install solar panels and systems for homes, businesses, and cities, with a goal to help reduce carbon emissions",
          src: imgSolaris,
          tags: [{ title: "Brand Design", bgColor: "#c5460026", color: "#c54600" }]
        },
        {
          title: "Time Keepers",
          description: "TimeKeepers is a company that specializes in time-travel technology. They offer exclusive trips to different eras in history, enabling customers to witness significant events and meet historical figures firsthand.",
          src: imgTimeKeep,
          tags: [{ title: "Communication Design", bgColor: "#A1C8CA26", color: "#A1C8CA" }]
        },
        {
          title: "Beyond",
          description: "Beyond is a fictional company that specializes in sustainable and eco-friendly solutions for the world's water crisis. They develop and implement water filtration systems, desalination technology,and irrigation systems that support agriculture",
          src: imgBeyond,
          tags: [{ title: "UX Research", bgColor: "#E6913B26", color: "#C54600" }, { title: "UX Writer", bgColor: "#41A93F26", color: "#41A93F" }]
        },
        {
          title: "Echo Dynamics",
          description: "Echo Dynamics is a company that designs and manufactures advanced sound systems for music enthusiasts and professionals. Their cutting-edge technology delivers high-quality sound experiences, making their products a popular choice ",
          src: imgEcho,
          tags: [{ title: "Digital Marketer", bgColor: "#6260DD26", color: "#6260DD" }]
        },
        {
          title: "Neo Health",
          description: "NeoHealth is a healthcare company that focuses on the development of personalized medicine. They use genetic testing and other advanced technologies to offer patients customized treatment plans based on their unique genetic makeup, medical history, and life",
          src: imgNeo,
          tags: [{ title: "Product Design", bgColor: "#1C1F3226", color: "#1C1F32" }]
        },
      ]
    }
  }
}
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Manrope");
/* @import url("~/assets/css/index.css"); */

.body {
  font-family: Manrope, sans-serif;
  margin: 0;
  /* overflow-x: hidden; */
  letter-spacing: -0.02em;
  transition: 0.5s;
}

@media screen and (min-width: 768px) {
  .header-text {
    margin: 0rem 10rem;
  }
}

@media screen and (min-width: 1024px) {
  .header-text {
    margin: 0rem 900px;
  }
}

li {
  list-style-type: none;
}

.footer-header {
  font-weight: 700;
  letter-spacing: -0.3px;
  font-size: 20px;
  color: #1C1F32;
  margin-bottom: 12px;
}

footer li {
  margin-bottom: 10px;
  color: #1E1E1ECC;
  font-size: 16px;
  font-weight: 600;
}

#hero .number-box {
  box-shadow: 0px 4px 25px 0px #1E1E1E0A;
}

#hero .number {
  color: #43437A;
  font-size: 40px;
  font-weight: 700;
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

.button:hover {
  background: linear-gradient(90.13deg, #6260DD -16.47%, #1C1F32 9.91%, #43437A 100.77%, rgba(98, 96, 221, 0.74) 124.22%);
}

.button:hover img {
  content: "";
  padding-left: 5px;
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
  font-size: 3rem;
  font-weight: 700;
  text-align: center;
  color: #1C1F32;
  margin: 0px 1rem;
  background-color: white;
  background-image: linear-gradient(93.66deg, #1C1F32 -1.44%, #1C1F32 -1.43%, #6260DD 76.08%);
  -webkit-text-fill-color: transparent;
  background-clip: text;
  -webkit-background-clip: text;
  -moz-background-clip: text;
}

.discover-card {
  padding: 1.5rem 1.25rem;
  background: white;
}

.discover-card:focus,
.discover-card:hover {
  outline: 2px solid rgba(67, 67, 122, 1);
  box-shadow: 0px 2px 25px 0px #1E1E1E1A;
  border-radius: 20px;
}

.discover-card:hover .discover-card-header>img {
  padding-left: 15px;
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

#today-job .header-text {
  margin: 0;
  text-align: left;
}

.job-card {
  background: white;
  border: 0.5px solid #1E1E1E80;
  box-shadow: 0px 1px 5px 0px #1E1E1E26;
  padding: 18px 16px;
}

.job-card-image {
  width: 60px;
}

.job-card-header {
  color: #1e1e1ecc;
  font-weight: 700;
  font-size: 20px;
}

.job-card-text {
  color: #1e1e1ecc;
  font-weight: 600;
  font-size: 16px;
}

.job-card-tag {
  padding: 4px 12px;
  margin-right: 10px;
  border-radius: 20px;
  font-weight: 600;
  font-size: 11px;
}
</style>
