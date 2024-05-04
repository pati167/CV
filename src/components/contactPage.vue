<template>
  <div>
    <div><h1>Get in Touch!</h1></div>
    <div>
      <img src="" alt="" />
      <img :src="githubContactIcon" alt="" />
      <img :src="cvContactIcon" alt="" />
    </div>
    <div><h1>Thank You.</h1></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      emailContactIcon: "./public/email.png",
      githubContactIcon: "./public/github.png",
      cvContactIcon: "./public/cv.png",
    };
  },
};
</script>
