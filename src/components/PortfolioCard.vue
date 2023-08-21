<template>
  <div>
    <img
      :src="imgUrl"
      :alt="title"
      class="max-w-[438x]"
    />
    <div>
      <h3 class="font-bold">{{ title }}</h3>
      <h3>{{ category }}</h3>
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
