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
      <div>
        <i class="text-center absolute w-4 sm:w-6 mt-[5px] ml-3 sm:ml-5"><img src="~/assets/svg/search.svg"
            class="inline"></i>
        <input type="search" name="search-bar" id="search-bar" placeholder="Search by company name or role..." disabled
          class="rounded-3xl w-full sm:w-[340px] pl-10 sm:pl-14 py-2 leading-tight bg-[#ECEDEB33] border border-[#A1C8CA] placeholder:text-sm sm:placeholder:text-base" />
      </div>
      <div class="flex flex-row flex-wrap justify-around gap-4 gap-y-8">
        <div v-for="card in discover_cards" class="discover-card w-4/5 md:w-5/12 xl:w-1/4">
          <div class="discover-card-image">
            <img :src="card.src" :alt="`${card.title} icon`" class="" />
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

    <section id="for-candidate"
      class="flex flex-col gap-8 justify-center items-start mx-4 sm:mx-8 lg:mx-20 mt-28 px-4 sm:px-8 lg:px-16 py-12">
      <h1 class="header-tag">
        For Candidate
      </h1>
      <p class="header-text">
        Create your profile for free and start now
      </p>
      <div class="flex flex-row flex-nowrap justify-between self-stretch gap-8 lg:gap-x-16 overflow-x-scroll p-0 m-0">
        <div v-for="card in candidate_cards"
          class="flex flex-col bg-white flex-shrink-0 justify-between items-stretch rounded-3xl w-full sm:w-full md:w-3/5 lg:w-1/3">
          <div class="blurred bg-fuchsia-100 h-60 border-0 w-full">
          </div>
          <div class="px-4">
            <p class="text-2xl text-[#1E1E1E] font-semibold my-3">{{ card.title }}</p>
            <p class="text-sm text-[#1E1E1E] font-semibold opacity-50 mb-4">
              {{ card.description }}
            </p>
            <button type="button"
              class="bg-[#F0F0F9] text-[#6260DD] text-sm font-bold rounded-xl px-4 py-1 mb-10 whitespace-nowrap hover:bg-[#6260DD] hover:text-white">
              <span class="pr-2">{{ card.btn_text }}</span><svg class="inline fill-[#6260DD]" width="14" height="13"
                viewBox="0 0 14 13" xmlns="http://www.w3.org/2000/svg">
                <path
                  d="M14 6.73908C13.9951 6.21297 13.7832 5.70998 13.41 5.33908L9.12 1.03908C8.93264 0.852833 8.67919 0.748291 8.415 0.748291C8.15081 0.748291 7.89736 0.852833 7.71 1.03908C7.61627 1.13205 7.54188 1.24265 7.49111 1.36451C7.44034 1.48637 7.4142 1.61707 7.4142 1.74908C7.4142 1.88109 7.44034 2.0118 7.49111 2.13366C7.54188 2.25552 7.61627 2.36612 7.71 2.45908L11 5.73908H1C0.734784 5.73908 0.48043 5.84444 0.292893 6.03197C0.105357 6.21951 0 6.47386 0 6.73908C0 7.00429 0.105357 7.25865 0.292893 7.44618C0.48043 7.63372 0.734784 7.73908 1 7.73908H11L7.71 11.0291C7.5217 11.2161 7.41538 11.4702 7.41444 11.7355C7.41351 12.0009 7.51802 12.2558 7.705 12.4441C7.89198 12.6324 8.1461 12.7387 8.41146 12.7396C8.67683 12.7406 8.9317 12.636 9.12 12.4491L13.41 8.14908C13.7856 7.77573 13.9978 7.26865 14 6.73908Z" />
              </svg>
            </button>
          </div>
        </div>
      </div>
    </section>

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
      class="flex flex-col gap-8 justify-center items-start mx-4 sm:mx-8 lg:mx-20 mt-28 px-4 sm:px-8 lg:px-16 py-12">
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
      <div class="flex flex-row flex-wrap justify-center lg:justify-between items-stretch gap-y-8 gap-x-8 mt-4">
        <div v-for="card in job_cards"
          class="job-card flex flex-col justify-around rounded-3xl w-full md:w-5/12 xl:w-1/4">
          <div class="job-card-image mb-6">
            <img :src="card.src" :alt="card.title + ' logo'">
          </div>
          <div class="job-card-header font-bold text-xl mb-3">
            {{ card.title }}
          </div>
          <div class="job-card-text font-semibold text-base mb-3">
            {{ card.description }}
          </div>
          <div class="flex flex-wrap flex-row">
            <span v-for="tag in card.tags" class="job-card-tag" :class="`bg-[${tag.bgColor}] text-[${tag.color}]`">
              {{ tag.title }}
            </span>
          </div>
        </div>
      </div>
    </section>

    <section class="flex flex-col gap-8 justify-center mx-8 md:mx-16 mt-28 items-center">
      <h1 class="header-tag">
        Our podcast
      </h1>
      <p class="header-text">
        Hear what we have to say about our openings
      </p>
      <div class="flex flex-wrap flex-row justify-between gap-8 lg:gap-16">
        <div v-for="card in podcast_cards" class="w-full md:w-5/12 xl:w-1/4">
          <div class="bg-black h-[455px] rounded-3xl"></div>
          <p class="text-2xl text-[#1C1F32] font-bold mt-4 px-2">{{ card.name }}</p>
          <p class="text-base font-bold text-[#1E1E1E80] mt-4 px-2">{{ card.description }}</p>
        </div>
      </div>
    </section>

    <footer class="flex flex-col lg:flex-row lg:px-24 gap-4 lg:gap-12 justify-between py-14 px-10 mt-28 bg-[#FAFBFA]">
      <div class="mb-10">
        <img src="~/assets/images/icon.png" class="inline absolute mt-0.5 w-8" alt="">
        <p class="inline ml-10 text-2xl">Creativepay</p>
      </div>
      <div class="grid grid-flow-row grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-8">
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

import imgUI from "~/assets/images/discover/ui_designer.png"
import imgVisual from "~/assets/images/discover/visual_animator.png"
import imgArt from "~/assets/images/discover/art_director.png"
import imgFont from "~/assets/images/discover/font_designer.png"
import imgFront from "~/assets/images/discover/front_dev.png"
import imgBack from "~/assets/images/discover/back_dev.png"
import imgUX from "~/assets/images/discover/ux_research.png"
import img3D from "~/assets/images/discover/3d_designer.png"
import imgGraphics from "~/assets/images/discover/graphics_designer.png"

import imgBQ from "~/assets/images/opportunities/bq_ltd.png"
import imgBeyond from "~/assets/images/opportunities/beyond.png"
import imgEcho from "~/assets/images/opportunities/echo_dyn.png"
import imgNeo from "~/assets/images/opportunities/neo_health.png"
import imgSolaris from "~/assets/images/opportunities/solaris.png"
import imgTimeKeep from "~/assets/images/opportunities/time_keep.png"

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
      ],
      candidate_cards: [
        {
          title: "Create Account",
          description: "Once the sign-up process is tested and working, you can start promoting your application to potential users and directing them to the sign-up page/form.",
          btn_text: "Create Account",
          image: "",
        },
        {
          title: "Search Roles",
          description: "Once the sign-up process is tested and working, you can start promoting your application to potential users and directing them to the sign-up page/form.",
          btn_text: "Browse roles",
          image: "",
        },
        {
          title: "Speak to recuiters",
          description: "Once the sign-up process is tested and working, you can start promoting your application to potential users and directing them to the sign-up page/form.",
          btn_text: "Send Proposal",
          image: "",
        },
      ],
      podcast_cards: [
        {
          name: "Tumise Ayan",
          description: "Understanding work policy. Understanding term of service and contract ",
          image: ""
        },
        {
          name: "Adura perry",
          description: "The business of being creative. Managing work life  and personal personal life ",
          image: ""
        },
        {
          name: "Oluwanifemi",
          description: "Dealing with laid off and tips on getting getting back into the market",
          image: ""
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

/* very small screens like the Galaxy Fold */
@media screen and (max-width: 300px) {
  .header-text {
    font-size: 2rem !important;
  }
}

@media screen and (max-width: 768px) {
  .header-text {
    font-size: 2rem !important;
  }
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
  background: #FAFBFA;

}

#for-candidate .header-text,
#today-job .header-text {
  margin: 0;
  text-align: left;
}

#for-candidate .blurred {
  position: relative;
  border-radius: inherit;
}

#for-candidate .blurred::after {
  content: "";
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  height: 4rem;
  background: linear-gradient(to bottom, #fff0, #ffff);
}

#for-candidate button:hover>svg {
  margin-left: 5px;
  fill: white;
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
  white-space: nowrap;
}
</style>
