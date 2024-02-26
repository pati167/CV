<template>
  <Navbar @navigate="navigateToPage"></Navbar>
  <component :is="currentPage"></component>
</template>

<script>
import HomePage from "./components/homePage.vue";
import AboutPage from "./components/aboutPage.vue";
import SkillsPage from "./components/skillsPage.vue";
import ExperiencePage from "./components/experiencePage.vue";
import Navbar from "./components/navbar.vue";

export default {
  data() {
    return {
      currentPage: HomePage,
    };
  },
  components: {
    Navbar,
    HomePage,
    AboutPage,
    SkillsPage,
    ExperiencePage,
  },
  methods: {
    navigateToPage(pageName) {
      switch (pageName) {
        case "home":
          this.currentPage = HomePage;
          break;
        case "about":
          this.currentPage = AboutPage;
          break;
        case "skills":
          this.currentPage = SkillsPage;
          break;
        case "experience":
          this.currentPage = ExperiencePage;
          break;
      }
    },
  },
};
</script>
