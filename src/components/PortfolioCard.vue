<template>
  <div>
    <img
      :src="imgUrl"
      :alt="title"
      class="max-w-[438x]"
    />
    <div class="mt-8">
      <h3 class="font-inter text-sm">{{ category }}</h3>
      <h3 class="font-bold text-2xl">{{ title }}</h3>
    </div>
  </div>
</template>

<script>
export default {
  components: {
    name: "PortfolioCard",
  },
  props: {
    title: {
      type: String,
      require: true,
    },
    category: {
      type: String,
      require: true,
    },
    imgUrl: {
      type: String,
      require: true,
    },
  },
};
</script>
