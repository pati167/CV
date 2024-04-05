<template>
  <div class="topnavbar">
    <div class="logoContainer">
      <img :src="logoP" class="logo" />
    </div>
    <nav>
      <ul class="list">
        <li class="link"><a @click="goToPage('home')">Home</a></li>
        <li class="link"><a @click="goToPage('about')">About</a></li>
        <li class="link"><a @click="goToPage('skills')">Skills</a></li>
        <li class="link"><a @click="goToPage('experience')">Experience</a></li>
      </ul>
    </nav>
  </div>
  <div class="icon">
    <a href="https://github.com/pati167"
      ><img :src="githubImgPath" class="githubIcon"
    /></a>
    <a :href="pdfPath"><img :src="cvImgPath" class="cvIcon" /></a>
  </div>
</template>

<style>
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
}
.topnavbar * {
  display: inline;
}

.link {
  margin: 20px;
  color: #27374d;
  font-size: 24px;
  text-decoration: none;
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
    };
  },
  methods: {
    goToPage(pageName) {
      this.$emit("navigate", pageName);
    },
  },
};
</script>
