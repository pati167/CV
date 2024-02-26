<template>
  <div class="topnavbar">
    <ul class="list">
      <li class="link"><a @click="goToPage('home')">Home</a></li>
      <li class="link"><a @click="goToPage('about')">About</a></li>
      <li class="link"><a @click="goToPage('skills')">Skills</a></li>
      <li class="link"><a @click="goToPage('experience')">Experience</a></li>
    </ul>
  </div>
</template>

<style>
.topnavbar {
  position: fixed;
  top: 25px;
  left: 510px;
}
.list {
  list-style-type: none;
  padding: 0;
  margin: 0;
  display: flex;
  justify-content: center;
}
.list :hover {
  color: #61788f;
}
.link {
  margin: 0 10px;
  color: #8ca4bc;
  padding-right: 18px;
}
.link:not(:last-child) {
  border-right: 2px solid #8ca4bc;
}

.topnavbar a {
  text-decoration: none;
  font-size: 25px;
  padding: 16px;
}
</style>

<script>
export default {
  methods: {
    goToPage(pageName) {
      this.$emit("navigate", pageName);
    },
  },
};
</script>
