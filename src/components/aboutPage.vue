<template>
  <div class="aboutContainer">
    <img :src="profileImagemPath" class="profileImg" />
    <h2 class="profileText">Hi im patricia and i love luna</h2>
  </div>
</template>

<style>
.aboutContainer {
  position: relative;
}
.profileImg {
  border-radius: 100%;
  width: 300px;
  position: absolute;
  right: 210px;
  top: -150px;
}
.profileText {
  position: relative;
  left: 450px;
  color: #61788f;
}
</style>

<script>
export default {
  data() {
    return {
      profileImagemPath: "/profile.jpeg",
    };
  },
};
</script>
