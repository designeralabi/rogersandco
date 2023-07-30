<script setup>
defineProps({
  brandCategory: String,
  brandTitle: String,
  more: String,

  brandBg: String,
  brandImage: String,
});
</script>

<template>
  <div>
    <div>
      <h3>{{ brandCategory }}</h3>
      <h2>{{ brandTitle }}</h2>
      <h2>{{ more }}</h2>
    </div>
    <img
      :src="brandImage"
      :alt="brandCategory"
    />
  </div>
</template>
