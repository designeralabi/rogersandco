<template>
  <div>
    <!-- hero section -->
    <AppHeader />
    <!-- main_hero -->
    <div
      class="w-full p-[98px] h-[368px] flex items-center justify-center bg-[url('./assets/teamwork_bg.png')] bg-no-repeat bg-cover relative"
    >
      <div
        class="bg-black/80 top-0 bottom-0 left-0 right-0 w-full absolute h-full z-10"
      ></div>
      <h3 class="text-center text-[28px] font-bold z-30">Contact</h3>
    </div>

    <!-- form -->
    <div class="flex items-center">
      <form class="p-[48px] font-bold bg-slate-400/20 w-full">
        <h2 class="text-2xl text-center">Got a Question? Write Us a Message</h2>
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
      <div>
        <ContactCard>
          <div class="bg-[#E9DDFF]">
            <div>
              <AnFilledPhone />
              <h3>Phone:</h3>
            </div>
          </div>
        </ContactCard>
      </div>
    </div>

    <!-- footer -->
    <footerCard />
  </div>
</template>

<script>
// AppHeader
import AppHeader from "../components/AppHeader.vue";
// footer
import footerCard from "../components/FooterCard.vue";
// contact_card
import ContactCard from "../components/ContactCard.vue";

import { AnFilledPhone } from "@kalimahapps/vue-icons";

export default {
  components: {
    AppHeader,
    footerCard,
    ContactCard,
    AnFilledPhone,
  },
};
</script>
