<script>
import { AkChevronRight } from "@kalimahapps/vue-icons";
export default {
  components: {
    AkChevronRight,
  },
  props: {
    brandCategory: String,
    brandTitle: String,
    more: String,
    brandBg: String,
    brandImage: String,
  },
};
</script>

<template>
  <div
    class="shadow-md flex items-center justify-center text-black max-w-[464.586px] rounded-md p-[14.268px]"
    :style="{ backgroundColor: brandBg }"
  >
    <div>
      <h3 class="uppercase">{{ brandCategory }}</h3>
      <h2 class="font-bold w-[202.42px] my-[26px]">{{ brandTitle }}</h2>
      <h3 class="cursor-pointer">
        <a
          href="#"
          class="text-[#60678E] flex items-center"
          >find out more <span class="ml-10"> <AkChevronRight /></span>
        </a>
      </h3>
    </div>
    <img
      :src="brandImage"
      class="w-[222.93px] h-[161.005px]"
    />
  </div>
</template>
    s