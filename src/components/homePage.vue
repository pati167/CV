<template>
  <head>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Raleway:ital,wght@0,100..900;1,100..900&display=swap"
      rel="stylesheet"
    />
  </head>
  <div class="homeText">
    <h1 class="patriciaGomes">Patrícia Gomes</h1>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>

<style>
.homeText {
  position: fixed;
}
.patriciaGomes {
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 100px;
  color: #b25068;
  font-family: "Raleway", sans-serif;
}
</style>
