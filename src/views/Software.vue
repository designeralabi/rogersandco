<script>
// AppHeader
import AppHeader from "../components/AppHeader.vue";
// footer
import footerCard from "../components/FooterCard.vue";
// vue icons
import { AkLinkedInV1Fill } from "@kalimahapps/vue-icons";
import { AkFacebookFill } from "@kalimahapps/vue-icons";
import { AkTwitterFill } from "@kalimahapps/vue-icons";
// portfoliocard
import portfolioCard from "../components/PortfolioCard.vue";
// import images
import swish from "../assets/swish.png";
import mdocScan from "../assets/mdocScan.png";

export default {
  components: {
    name: "software",
    AppHeader,
    footerCard,
    portfolioCard,
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
      portfolios: [
        {
          title: "Swish",
          category: "Brand Identity & Development & Design | Web Application",
          imgUrl: swish,
        },
        {
          title: "Mdata solution",
          category: "SoftwareSoftware",
          imgUrl: mdocScan,
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
    <div class="space-y-7 p-[120px] mx-auto">
      <h1 class="text-7xl font-bold ml-24 max-w-[1500px]">Software</h1>
      <div class="flex justify-between">
        <h2 class="w-[703px] ml-24">
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
      <div class="py-[89px] pr-32">
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
          <div>
            <h3 class="text-2xl mb-8">Product Development</h3>
            <p>
              At Rogers & Co, our Software Product Development department sets
              the standard for excellence in the industry. Our team of expert
              developers and designers are dedicated to creating cutting-edge
              products that solve real-world problems and drive business
              success. With a focus on user-centered design and the latest
              technology, we deliver solutions that not only meet, but exceed
              expectations.
            </p>
          </div>
          <div>
            <h3 class="text-2xl mb-8">Software Development</h3>
            <p>
              At Rogers & Co, our Software Development team is composed of
              highly skilled and knowledgeable professionals who are dedicated
              to delivering innovative software solutions. Our process is guided
              by Agile methodologies, such as Scrum and Kanban, to ensure
              flexibility and responsiveness in response to the ever-changing
              needs of our clients.
            </p>
          </div>
        </div>
      </div>
    </div>
    <!-- related cases -->
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

    <div class="px-[140px] py-[100px]">
      <div class="max-w-5xl flex gap-x-24 mx-auto">
        <div class="items-start w-full">
          <h3 class="font-bold">Adesokan & Adesokan</h3>
          <h3>Adesokan & Adesokan LLP</h3>
          <h3>Managing Partner</h3>
        </div>
        <div class="">
          <h3>
            "Embracing an Electronic Document Management System (EDMS) was a
            game-changer for our organization. The seamless transition from
            paper to digital documents not only streamlined our workflow but
            also revolutionized how we collaborate. Retrieving crucial
            information now takes seconds, not hours, boosting our efficiency
            and productivity. The EDMS service has truly empowered us to work
            smarter and faster, making it an indispensable asset for our
            business."
          </h3>
        </div>
      </div>
    </div>

    <div class="bg-white pl-[140px]">
      <div class="bg-[#F0F0F0] py-[90px]">
        <h3 class="text-4xl pl-[100px]">
          Contact us if you want to hear more about how we can help with your
          project
        </h3>
      </div>
    </div>
  </div>
</template>
