<template>
  <img :src="profileImagemPath" class="profileImg" />
  <div class="textContainer">
    <h1 class="profileTitle">Hello!</h1>
    <h2 class="profileText">
      I’m an aspiring front-end developer, eager to dive into the world of
      coding.<br /><br />
      <span class="boldText">
        With a passion for problem-solving and a love for creativity, I'm
        excited to learn the ins and outs of web development. </span
      ><br />
      <br />Although I'm new to the field, I'm dedicated to mastering HTML, CSS,
      and JavaScript to build sleek and functional websites. I'm constantly
      seeking new challenges and opportunities to grow my skills.
    </h2>
  </div>
</template>

<style>
.profileImg {
  position: fixed;
  left: 250px;
  bottom: 200px;
  width: 400px;
  box-shadow: 30px 30px #526d82;
  border-top-right-radius: 20px;
}
.textContainer {
  position: absolute;
  width: 420px;
  right: 750px;
  bottom: 220px;
}

.profileTitle {
  position: relative;
  font-family: "Montserrat", sans-serif;
  font-weight: 700;
  font-style: normal;
  font-size: 30px;
  color: #27374d;
  left: 450px;
  margin-bottom: 10px;
}

.profileText {
  position: relative;
  left: 450px;
  color: #27374d;
  font-family: "Montserrat", sans-serif;
  font-weight: 400;
  font-style: normal;
  font-size: 16px;
}
.boldText {
  font-weight: 700;
  font-size: 20px;
}
</style>

<script>
export default {
  data() {
    return {
      profileImagemPath: "/profile.png",
    };
  },
};
</script>
