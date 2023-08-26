<template>
  <div>
    <!-- hero section -->
    <AppHeader />
    <!-- <navBar /> -->
    <div class="space-y-7 p-[120px] mx-auto">
      <h1 class="text-7xl font-bold ml-24 max-w-[1500px]">
        Transforming Possibilities, <br />
        Using Software and Hardware <br />
        to Redefine the Future
      </h1>
      <div class="flex justify-between">
        <h2 class="w-[703px] ml-24">
          Strategy, technological innovation, and hardware integration form the
          fundamental building blocks in crafting robust solutions that enhance
          the operational framework of our clients' enterprises.
        </h2>

        <div class="flex items-center gap-x-10">
          <a
            href="#"
            class="hover:text-gray-400 transition-colors"
          >
            <AkLinkedInV1Fill class="text-2xl cursor-pointer"
          /></a>
          <a
            href="#"
            class="hover:text-gray-400 transition-colors"
          >
            <AkFacebookFill class="text-2xl"
          /></a>
          <a
            href="#"
            class="hover:text-gray-400 transition-colors"
          >
            <AkTwitterFill class="text-2xl"
          /></a>
        </div>
      </div>
    </div>

    <!-- hero_media  -->
    <div class="relative">
      <div
        class="absolute bg-black/30 z-20 top-0 left-0 right-0 bottom-0"
      ></div>
      <div class="w-full pl-[170px]">
        <video
          muted="muted"
          loop="loop"
          playsinline=""
          preload="auto"
          autoplay
          class="w-full"
        >
          <source
            :src="rogersVid"
            type="video/mp4"
          />
        </video>
      </div>
    </div>

    <!-- brands -->
    <div
      class="py-[300px] px-[120px] bg-[#F0F0F0] flex justify-center items-center h-screen"
    >
      <div class="max-w-[1100px] mx-auto">
        <h1 class="font-extrabold leading-normal text-2xl">
          Rogers & Co. is a leading technology organization at the forefront of
          delivering seamless solutions for both software and hardware projects.
          With a proven track record of excellence, we are dedicated to guiding
          our clients through every step of their technological journey.
        </h1>
      </div>
    </div>
    <!-- Relevant cases -->
    <div class="pl-[170px] bg-white -z-10 relative">
      <div class="z-30 pb-[170px]">
        <h2 class="text-5xl pl-[120px] z-40 mb-[50px]">Relevant cases</h2>
        <div class="grid grid-cols-3 gap-y-24">
          <portfolioCard
            v-for="portfolio in portfolios"
            :key="portfolio.title"
            :title="portfolio.title"
            :category="portfolio.category"
            :imgUrl="portfolio.imgUrl"
          />
        </div>
      </div>
      <div
        class="bg-[#F0F0F0] h-[230px] block absolute top-0 -z-20 w-full left-0 right-0"
      ></div>
    </div>

    <!-- testimonials -->
    <!-- <div class="py-[137px]">
      <h3 class="text-center text-3xl font-bold my-16">Testimonials</h3>
      <div
        class="grid gap-x-[52px] overflow-x-scroll grid-cols-3 max-w-[1155px] mx-auto"
      >
        <testimonialCard
          v-for="testimonial in testimonials"
          :key="testimonial.name"
          :name="testimonial.name"
          :content="testimonial.content"
          :company="testimonial.company"
        />
      </div>
    </div> -->
    <div class="bg-[#979A9D] text-white px-[170px] py-[120px]">
      <h1 class="text-5xl mb-[50px]">Services</h1>
      <div class="flex justify-between font-inter">
        <h3>What we offer</h3>
        <div class="bg-white h-[2px] w-20"></div>
        <p class="max-w-[630px] px-12">
          At our company, we take pride in offering a comprehensive range of
          cutting-edge services to meet the diverse needs of our clients. Our
          software division excels in providing top-notch solutions, including
          innovative design, seamless product development, and robust software
          and hardware engineering. In the realm of hardware, we specialize in
          two vital areas: security and renewable energy. Our dedicated security
          experts employ the latest technologies to fortify your systems and
          safeguard your valuable data.
        </p>
      </div>
    </div>

    <div class="bg-white pl-[170px] -z-10 relative">
      <div class="flex">
        <div class="bg-[#FDDDD1] w-full h-[650px]"></div>
        <div class="bg-[#C1CACE] w-full h-[650px]"></div>
      </div>
      <div
        class="bg-[#979A9D] h-[230px] block absolute top-0 -z-20 w-full left-0 right-0"
      ></div>
    </div>

    <!-- clients section -->
    <div class="bg-white">
      <div class="px-[170px] py-[120px]">
        <h1 class="text-3xl mb-[50px]">selection of our clients</h1>
      </div>
    </div>

    <!-- footer -->
    <footerCard />
  </div>
</template>

<script>
import BrandCard from "../components/BrandCard.vue";
import { AkChevronRight } from "@kalimahapps/vue-icons";
import portfolioCard from "../components/PortfolioCard.vue";
import testimonialCard from "../components/TestimonialCard.vue";
// AppHeader
import AppHeader from "../components/AppHeader.vue";

// footer
import footerCard from "../components/FooterCard.vue";
// brandCategory
import websiteDesign from "../assets/website_design.png";
import productDevelopment from "../assets/product_development.png";
import softwareDevelopment from "../assets/software_development.png";
import hardWare from "../assets/security_solar.png";
// brandImages
import yato from "../assets/yato.png";
import swish from "../assets/swish.png";
import mdataSolution from "../assets/mdata_solutions.png";
import mdocScan from "../assets/mdocScan.png";
// video
import rogersVid from "../assets/video/rogers&Co.mp4";

// vue icons
import { AkLinkedInV1Fill } from "@kalimahapps/vue-icons";
import { AkFacebookFill } from "@kalimahapps/vue-icons";
import { AkTwitterFill } from "@kalimahapps/vue-icons";

export default {
  components: {
    name: "Home",
    BrandCard,
    AkChevronRight,
    portfolioCard,
    testimonialCard,
    AppHeader,
    footerCard,
    // vue_icons_component
    AkLinkedInV1Fill,
    AkFacebookFill,
    AkTwitterFill,
  },
  data() {
    return {
      rogersVid,
      brands: [
        {
          brandCategory: "Design",
          brandTitle: "Website Design & Design Thinking",
          more: "Find out more",
          brandBg: "#60678E",
          brandImage: websiteDesign,
        },
        {
          brandCategory: "Product",
          brandTitle: "Product Des ign & Development",
          more: "Find out more",
          brandBg: "#D6EDFF",
          brandImage: productDevelopment,
        },
        {
          brandCategory: "Software",
          brandTitle: "Software Development",
          more: "Find out more",
          brandBg: "#FFEDE1",
          brandImage: softwareDevelopment,
        },
        {
          brandCategory: "Hardware",
          brandTitle: "Security & Solar Power Systems",
          more: "Find out more",
          brandBg: "#FFD6D6",
          brandImage: hardWare,
        },
      ],
      portfolios: [
        {
          title: "Profitable",
          category: "Corporate Website | Web Application",
          imgUrl: yato,
        },
        {
          title: "Swish",
          category: "Brand Identity & Development & Design | Web Application",
          imgUrl: swish,
        },
        {
          title: "LiveSmart",
          category: "Design",
          imgUrl: mdataSolution,
        },
        {
          title: "Mdata solution",
          category: "SoftwareSoftware",
          imgUrl: mdocScan,
        },
        {
          title: "Osborne Towers",
          category:
            "Audio, Video, Lighting, Climate control and home automation.",
          imgUrl: yato,
        },
        {
          title: "Nycil Limited",
          category: "IP Video Surveillance",
          imgUrl: yato,
        },
      ],
      testimonials: [
        {
          name: "Ayodeji Aderoju",
          content:
            "I love how they synced with our internal team / process. Very impressed by the quality of their work too.",
          company: "yato",
        },
        {
          name: "Adeyemi Afolayan",
          content:
            "I love how they synced with our internal team / process. Very impressed by the quality of their work too.",
          company: "yato",
        },
        {
          name: "Dotun Afolayan",
          content:
            "I love how they synced with our internal team / process. Very impressed by the quality of their work too.",
          company: "yato",
        },
      ],
      clients: [
        {
          imgPath
        }
      ]
    };
  },
};
</script>
