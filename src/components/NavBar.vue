<template>
  <div>
    <h2>Logo</h2>
    <!-- <nav>
      <router-link to="/">Go to Home</router-link>
      <router-link to="about">Go to Home</router-link>
      <router-link to="software">Go to Home</router-link>
      <router-link to="hardware">Go to Home</router-link>
      <router-link to="contact">Go to Home</router-link>
      <router-view></router-view>
    </nav> -->
  </div>
</template>

<script>
export default {
  components: {
    NavBar
  },
  data() {
    return {
      title: "header nav",
    };
  },
};
</script>
