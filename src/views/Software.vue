<script>
// AppHeader
import AppHeader from "../components/AppHeader.vue";
// footer
import footerCard from "../components/FooterCard.vue";

export default {
  components: {
    name: "software",
    AppHeader,
    footerCard,
  },
};
</script>

<template>
  <div>
    <!-- hero section -->
    <AppHeader />
    <!-- <navBar /> -->
    <div class="space-y-7 py-[247px] pl-64 max-w-[1255px] mx-auto">
      <h1 class="text-6xl font-bold">Software</h1>
      <div class="flex justify-between">
        <h2 class="w-[473px]">
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

    <div class="bg-[#979A9D] text-white pl-64">
      <div class="py-20 pr-32">
        <h3 class="text-4xl my-8">Design</h3>
        <div class="flex gap-x-28">
          <div class="flex justify-between gap-x-11  bg-red-400 items-start">
            <span class="w-full">What we offer</span>
            <span class="h-[2px] w-24 bg-white"></span>
          </div>
          <div>
            <p>
              The Rogers & Co. design team is dedicated to re-imagining how
              brands, businesses and organizations are perceived. We specialize
              in bringing digital identities into the real world. While very
              diverse, our aesthetic approach often involves a distinct sense of
              style and design, aiming to combine out-of-the-box design with
              functionality. Strategically, our work aims to elevate brand
              offerings by distilling core messaging down to its clearest and
              freshest visual form.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
