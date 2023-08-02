<template>
  <div>
    <!-- hero section -->
    <AppHeader />
    <!-- footer -->
    <footerCard />
  </div>
</template>

<script>
// AppHeader
import AppHeader from "../components/AppHeader.vue";
// footer
import footerCard from "../components/FooterCard.vue";

export default {
  components: {
    AppHeader,
    footerCard,
  },
};
</script>
