<script setup>
import BrandCard from "../components/BrandCard.vue";
let brands = [
  {
    brandCategory: "Design",
    brandTitle: "Website Design & Design Thinking",
    more: "Find out more",
    brandBg: "",
    brandImage: "",
  },
  {
    brandCategory: "Product",
    brandTitle: "Product Design & Development",
    more: "Find out more",
    brandBg: "",
    brandImage: "",
  },
  {
    brandCategory: "Software",
    brandTitle: "Software Development",
    more: "Find out more",
    brandBg: "",
    brandImage: "",
  },
  {
    brandCategory: "Hardware",
    brandTitle: "Security & Solar Power Systems",
    more: "Find out more",
    brandBg: "",
    brandImage: "",
  },
];
console.log(brands.brandCategory);
</script>

<template>
  <div>
    <!-- hero section -->
    <div>
      <h1>Innovation made simple</h1>
      <h2>Innovate, transform, succeed with us.</h2>
      <button>Get Started Today</button>
    </div>

    <!-- brands -->
    <div>
      <BrandCard
        v-for="(brand, index) in brands"
        key="index"
        brandCategory="brand.brandCategory"
        brandTitle="sing"
        brandBg="red"
        brandImage="welcome sin"
      />
    </div>
  </div>
</template>
