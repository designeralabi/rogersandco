<script>
// AppHeader
import AppHeader from "../components/AppHeader.vue";
// footer
import footerCard from "../components/FooterCard.vue";
// vue icons
import { AkLinkedInV1Fill } from "@kalimahapps/vue-icons";
import { AkFacebookFill } from "@kalimahapps/vue-icons";
import { AkTwitterFill } from "@kalimahapps/vue-icons";

export default {
  components: {
    name: "software",
    AppHeader,
    footerCard,
    // vue_icons_component
    AkLinkedInV1Fill,
    AkFacebookFill,
    AkTwitterFill,
  },
  data() {
    return {
      heroCards: [
        {
          title: "card 1",
          color: "#ffffff",
          textColo: "#000",
        },
        {
          title: "card 2",
          color: "#000000",
        },
        {
          title: "card 3",
          color: "#ffffff",
          textColo: "#000",
        },
        {
          title: "card 4",
          color: "#000000",
        },
        {
          title: "card 5",
          color: "#000000",
        },
        {
          title: "card 6",
          color: "#ffffff",
          textColo: "#000",
        },
        {
          title: "card 7",
          color: "#000000",
        },
        {
          title: "card 8",
          color: "#ffffff",
          textColo: "#000",
        },
      ],
    };
  },
};
</script>

<template>
  <div>
    <!-- hero section -->
    <AppHeader />
    <!-- <navBar /> -->
    <div class="space-y-7 pt-[247px] pl-64 max-w-[1255px] mx-auto">
      <h1 class="text-6xl font-bold">Software</h1>
      <div class="flex justify-between">
        <h2 class="w-[473px]">
          We develop tailored, complex web applications and systems in the form
          of applications, online services, apps, intranets and extranets.
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
    <div class="grid grid-cols-4 pl-64 mt-24">
      <div
        v-for="card in heroCards"
        :key="card.title"
        class="w-[325px] h-[267px] flex items-center justify-center"
        :style="{ backgroundColor: card.color }"
      >
        <h3
          class="text-white"
          :style="{ colors: card.textColor }"
        >
          {{ card.title }}
        </h3>
      </div>
    </div>

    <div class="bg-[#F0F0F0] text-black pl-64">
      <div class="py-20 pr-32">
        <h3 class="text-4xl my-8">Our Services</h3>
        <div class="flex gap-x-28 mt-16 justify-between items-start">
          <div>
            <h3 class="text-2xl mb-8">Design</h3>
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
