<template>
  <div>
    <!-- hero section -->
    <AppHeader />
    <!-- <navBar /> -->
    <div class="text-center space-y-7 py-[247px]">
      <h1 class="text-[40px] font-bold">Innovation made simple</h1>
      <h2>Innovate, transform, succeed with us.</h2>
      <button
        class="flex items-center bg-[#FEF200] rounded-[40px] font-bold text-black py-[18px] px-[24px] mx-auto"
      >
        Get Started Today
      </button>
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
    <div class="py-36 bg-[#252533]">
      <h1 class="text-center font-extrabold text-3xl my-[40px]">
        We Help Brands with
      </h1>
      <div class="grid grid-cols-2 gap-7 my-[72px] mx-auto w-[980px]">
        <BrandCard
          v-for="(brand, index) in brands"
          :key="index"
          :brandCategory="brand.brandCategory"
          :brandTitle="brand.brandTitle"
          :brandBg="brand.brandBg"
          :brandImage="brand.brandImage"
        />
      </div>
      <div class="flex items-center gap-x-[43px] justify-center">
        <h2>Let’s Start A New Project Together</h2>
        <button
          class="flex items-center bg-[#FEF200] rounded-[40px] font-bold text-black py-[18px] px-[24px]"
        >
          request a Quote <span class="ml-4"> <AkChevronRight /></span>
        </button>
      </div>
    </div>

    <!-- portfolio -->
    <div class="pt-36">
      <h2 class="text-center text-2xl">portfolio</h2>
      <div
        class="flex items-center gap-x-[64px] mx-auto max-w-[672px] my-8 font-bold"
      >
        <h3 class="bg-[#FEF200] text-black p-4">All</h3>
        <h3>Software</h3>
        <h3>Hardware</h3>
      </div>
      <div
        class="grid grid-cols-3 max-w-[1048px] mx-auto gap-x-[147px] gap-y-[44px] mt-[80px]"
      >
        <portfolioCard
          v-for="portfolio in portfolios"
          :key="portfolio.title"
          :title="portfolio.title"
          :category="portfolio.category"
          :imgUrl="portfolio.imgUrl"
        />
      </div>
      <h3>see more</h3>
    </div>

    <!-- testimonials -->
    <div class="py-[137px]">
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
    </div>

    <!-- getStarted -->
    <div
      class="flex max-w-[1155px] mx-auto gap-x-[99px] Py-[580px] items-center"
    >
      <div>
        <h2 class="font-extrabold text-3xl my-[40px]">Get Started</h2>
        <hr />
        <h3 class="my-8">
          Join dozens of corporates, fast-growing startups scaling their teams,
          accessing new market opportunities and building brilliant products
          with the Rogers & Co. team.
        </h3>
      </div>
      <form class="p-[48px] font-bold bg-slate-400/20 w-full">
        <h2 class="text-2xl text-center">Tell us about your project</h2>
        <div class="flex flex-col space-y-6 mt-8">
          <input
            type="text"
            placeholder="fullname"
            class="w-full bg-transparent p-3 border-b placeholder:text-sm placeholder:-translate-y-2 placeholder:-translate-x-3 capitalize outline-none"
          />
          <input
            type="text"
            placeholder="company"
            class="w-full bg-transparent p-3 border-b placeholder:text-sm placeholder:-translate-y-2 placeholder:-translate-x-3 capitalize outline-none"
          />
          <input
            type="text"
            placeholder="email"
            class="w-full bg-transparent p-3 border-b placeholder:text-sm placeholder:-translate-y-2 placeholder:-translate-x-3 capitalize outline-none"
          />
          <input
            type="text"
            placeholder="message"
            class="w-full bg-transparent p-3 border-b placeholder:text-sm placeholder:-translate-y-2 placeholder:-translate-x-3 capitalize outline-none"
          />
        </div>
      </form>
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

export default {
  components: {
    name: "Home",
    BrandCard,
    AkChevronRight,
    portfolioCard,
    testimonialCard,
    AppHeader,
    footerCard,
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
          brandTitle: "Product Design & Development",
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
          title: "Yato",
          category: "Design",
          imgUrl: yato,
        },
        {
          title: "Swish",
          category: "Product",
          imgUrl: swish,
        },
        {
          title: "MData Solutions",
          category: "Design",
          imgUrl: mdataSolution,
        },
        {
          title: "MDocScan",
          category: "SoftwareSoftware",
          imgUrl: mdocScan,
        },
        {
          title: "Profitable",
          category: "Software",
          imgUrl: yato,
        },
        {
          title: "Security and Solar Projects",
          category: "Hardware",
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
    };
  },
};
</script>
