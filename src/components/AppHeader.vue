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
          class="w-[120px] invert"
        />
      </div>
      <nav class="flex items-center space-x-4 capitalize">
        <router-link to="/">Home</router-link>
        <router-link :to="{ name: 'about' }">about</router-link>
        <router-link :to="{ name: 'software' }">software</router-link>
        <router-link :to="{ name: 'hardware' }">hardware</router-link>
        <router-link :to="{ name: 'contact' }">contact</router-link>
      </nav>
    </div>
  </div>
</template>
