<template>
  <div>
    <img
      :src="imgUrl"
      :alt="title"
      class="w-[250.969px]"
    />
    <div>
      <h3 class="font-bold">{{ title }}</h3>
      <h3>{{ category }}</h3>
    </div>
  </div>
</template>

<script>
export default {
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
  components: {
    name: "PortfolioCard",
  },
};
</script>
