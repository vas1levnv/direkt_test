<template>
  <div class="main-content">
    <HomePage/>
    <div class="container">
      <AboutUs/>
      <CaseProjects :posts="posts"/>
    </div>
  </div>
</template>

<script>

import HomePage from "@/components/MainContent/HomePage";
import AboutUs from "@/components/MainContent/AboutUs";
import CaseProjects from "@/components/MainContent/CaseProjects";

export default {
  components: {
    HomePage,
    AboutUs,
    CaseProjects
  },
  props: {
    posts: {
      type: Array,
      required: true,
    }
  },

  name: "blackBackgroundContent"
}
</script>

<style scoped>
.main-content {
  background: #0E0E0E;
  color: #ffffff;
  padding-top: 120px;
  padding-bottom: 40px;
}


</style>