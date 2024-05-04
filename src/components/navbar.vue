<template>
  <div class="topnavbar">
    <div class="logoContainer">
      <img :src="logoP" class="logo" />
    </div>
    <nav>
      <ul class="list">
        <li :class="{ active: currentPage === 'home' }" class="link">
          <a @click="goToPage('home')">Home</a>
        </li>

        <li :class="{ active: currentPage === 'about' }" class="link">
          <a @click="goToPage('about')">About</a>
        </li>
        <li :class="{ active: currentPage === 'Experience' }" class="link">
          <a @click="goToPage('experience')">Experience</a>
        </li>
        <li :class="{ active: currentPage === 'skills' }" class="link">
          <a @click="goToPage('skills')">Skills</a>
        </li>
        <li :class="{ active: currentPage === 'contact' }" class="link">
          <a @click="goToPage('contact')">Contact</a>
        </li>
      </ul>
    </nav>
  </div>
  <div v-if="showIcons" class="icon">
    <a href="https://github.com/pati167"
      ><img :src="githubImgPath" class="githubIcon"
    /></a>
    <a :href="pdfPath"><img :src="cvImgPath" class="cvIcon" /></a>
  </div>
</template>

<style>
.link a.active {
  font-weight: bold;
}
.logoContainer {
  padding: 20px 50px 20px 30px;
  align-items: center;
  border-right: solid 3px #526d82;
}
.logo {
  height: 30px;
}
.topnavbar {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  padding: 20px;
  height: 80px;
  display: flex;
  align-items: center;
  border-bottom: solid 3px #526d82;
  background-color: #f6f1f1;
  z-index: 1000;
}
.topnavbar * {
  display: inline;
}

.link {
  margin: 20px;
  color: #27374d;
  font-size: 24px;
  text-decoration: none;
  font-family: "Montserrat", sans-serif;
  font-weight: 400;
  font-style: normal;
}
.link :hover {
  font-weight: bold;
}
.icon {
  position: fixed;
  bottom: 20px;
  left: 20px;
}
.githubIcon {
  width: 40px;
  height: 40px;
  margin-right: 5px;
  margin-bottom: 1px;
}
.cvIcon {
  height: 40px;
}
</style>

<script>
export default {
  data() {
    return {
      logoP: "/P.png",
      githubImgPath: "/github.png",
      cvImgPath: "/cv.png",
      pdfPath: "/Patricia_CV.pdf",
      currentPage: "home",
    };
  },
  props: {
    showIcons: {
      type: Boolean,
      default: true,
    },
  },
  methods: {
    goToPage(pageName) {
      this.currentPage = pageName;
      this.$emit("navigate", pageName);
    },
  },
};
</script>
