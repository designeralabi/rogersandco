<template>
  <div class="bg-blue-950/20 p-[24px] w-[368px]">
    <h3>{{ content }}</h3>
    <div class="mt-6">
      <h3>{{ name }}</h3>
      <h4 class="text-[#60678E]">{{ company }} - Nigeria</h4>
    </div>
  </div>
</template>

<script>
export default {
  components: {
    name: "TestimonialCard",
  },
  props: {
    name: {
      type: String,
      required: true,
    },
    content: {
      type: String,
      required: true,
    },
    company: {
      type: String,
      required: true,
    },
  },
};
</script>
