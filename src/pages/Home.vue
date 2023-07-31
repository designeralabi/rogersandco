<template>
  <div>
    <!-- hero section -->
    <div class="text-center space-y-7 py-[147px]">
      <h1 class="text-[40px] font-bold">Innovation made simple</h1>
      <h2>Innovate, transform, succeed with us.</h2>
      <button
        class="flex items-center bg-[#FEF200] rounded-[40px] font-bold text-black py-[18px] px-[24px] mx-auto"
      >
        Get Started Today
      </button>
    </div>

    <!-- brands -->
    <div class="py-16">
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
    <div>
      <h2 class="text-center text-2xl">portfolio</h2>
      <div
        class="flex items-center gap-x-[64px] mx-auto max-w-[672px] my-8 font-bold"
      >
        <h3 class="bg-[#FEF200] text-black p-4">All</h3>
        <h3>Design</h3>
        <h3>Product</h3>
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
    </div>

    <!-- testimonials -->
    <div class="p-[68px]">
      <h3 class="text-center text-2xl font-bold my-8">Testimonials</h3>
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
  </div>
</template>

<script>
import BrandCard from "../components/BrandCard.vue";
import { AkChevronRight } from "@kalimahapps/vue-icons";
import portfolioCard from "../components/portfolioCard.vue";
import testimonialCard from "../components/TestimonialCard.vue";

export default {
  components: {
    name: "Home",
    BrandCard,
    AkChevronRight,
    portfolioCard,
    testimonialCard,
  },
  data() {
    return {
      brands: [
        {
          brandCategory: "Design",
          brandTitle: "Website Design & Design Thinking",
          more: "Find out more",
          brandBg: "#60678E",
          brandImage: "/src/assets/website_design.png",
        },
        {
          brandCategory: "Product",
          brandTitle: "Product Design & Development",
          more: "Find out more",
          brandBg: "#D6EDFF",
          brandImage: "/src/assets/product_development.png",
        },
        {
          brandCategory: "Software",
          brandTitle: "Software Development",
          more: "Find out more",
          brandBg: "#FFEDE1",
          brandImage: "/src/assets/software_development.png",
        },
        {
          brandCategory: "Hardware",
          brandTitle: "Security & Solar Power Systems",
          more: "Find out more",
          brandBg: "#FFD6D6",
          brandImage: "/src/assets/security_solar.png",
        },
      ],
      portfolios: [
        {
          title: "Yato",
          category: "Design",
          imgUrl: "/src/assets/yato.png",
        },
        {
          title: "Swish",
          category: "Product",
          imgUrl: "/src/assets/swish.png",
        },
        {
          title: "MData Solutions",
          category: "Design",
          imgUrl: "/src/assets/mdata_solutions.png",
        },
        {
          title: "MDocScan",
          category: "SoftwareSoftware",
          imgUrl: "/src/assets/mdocScan.png",
        },
        {
          title: "Profitable",
          category: "Software",
          imgUrl: "/src/assets/yato.png",
        },
        {
          title: "Security and Solar Projects",
          category: "Hardware",
          imgUrl: "/src/assets/yato.png",
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
