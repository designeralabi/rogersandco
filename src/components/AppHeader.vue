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
  <div class="">
    <div class="flex items-center justify-between py-6 max-w-[1155px] mx-auto">
      <div>
        <img
          :src="imgPath"
          alt="logo"
          class="w-[120px]"
        />
      </div>
      <nav class="flex items-center space-x-4 capitalize">
        <router-link to="/">Home</router-link>
        <router-link :to="{ name: 'about' }">about</router-link>
        <router-link :to="{ name: 'software' }">software</router-link>
        <router-link :to="{ name: 'hardware' }">hardware</router-link>
        <router-link :to="{ name: 'contact' }">contact</router-link>
      </nav>
      <div>
        <div>
          <h3>
            E: <a href="mailto: info@rogersandco.xyz">info@rogersandco.xyz</a>
          </h3>
          <h3>T: +234(0)8169169966</h3>
        </div>
        <h3>A: 1637, Ademola Adetokunbo, VI, Lagos, Nigeria</h3>
      </div>
    </div>
  </div>
</template>
