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
  </div>
</template>
