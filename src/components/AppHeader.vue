<script>
import logo from "../assets/logo_800_white_background.png";
export default {
  data() {
    return {
      imgPath: logo,
    };
  },
};
</script>

<template>
  <div>
    <div
      class="flex items-center justify-between py-9 max-w-[1255px] mx-auto relative"
    >
      <div class="-rotate-90 absolute top-28">
        <h3 class="font-cardo text-3xl items-end">
          <router-link to="/">Rogers & Co.</router-link>
        </h3>
      </div>
      <nav class="flex gap-x-11 pl-64 items-center space-x-4 capitalize">
        <router-link :to="{ name: 'software' }">Cases</router-link>
        <router-link :to="{ name: 'about' }">About Us</router-link>

        <router-link :to="{ name: 'hardware' }">Services</router-link>
        <router-link :to="{ name: 'contact' }">contact</router-link>
      </nav>
      <div class="flex gap-x-8">
        <div>
          <h3 class="underline">
            E: <a href="mailto: info@rogersandco.xyz">info@rogersandco.xyz</a>
          </h3>
          <h3 class="underline">T: +234(0)8169169966</h3>
        </div>
        <h3>
          A: 1637, Ademola Adetokunbo, <br />
          VI, Lagos, Nigeria
        </h3>
      </div>
    </div>
  </div>
</template>
