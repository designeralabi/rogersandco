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
  <div class="bg-white">
    <div class="flex items-center justify-between py-2 max-w-[1155px] mx-auto">
      <div>
        <img
          :src="imgPath"
          alt="logo"
          class="w-[120px]"
        />
      </div>
      <div class="flex items-center space-x-4 capitalize">
        <router-link to="/">Home</router-link>
        <router-link to="/about">about</router-link>
        <router-link to="/software">software</router-link>
        <router-link to="/hardware">hardware</router-link>
        <router-link to="/contact">contact</router-link>
      </div>
    </div>
  </div>
</template>
