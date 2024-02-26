<template>
  <div class="studyContainer">
    <ul class="studyInventory">
      <h1 class="studyTitle">Study</h1>
      <li class="scholl studyList">
        <h2>Communication and Audiovisuals</h2>
        <p>Artistic School Antonio Arroio</p>
      </li>
      <li class="photographyCourse studyList">
        <h2>Photography Course</h2>
        <p>EPI, Escola Profissional de Imagem</p>
      </li>
      <li class="professionalTrainin studyList">
        <h2>Professional training - Centro de Alto Rendimento</h2>
        <p>Skills Gym, Centro de Competências</p>
      </li>
      <li class="EnglishCourse studyList">
        <h2>English Course</h2>
        <p>Skills Gym, Centro de Competências</p>
      </li>
      <li class="webDevelopmentCourse studyList">
        <h2>The Complete 2024 Web Development Bootcamp</h2>
      </li>
      <li class="JavascriptCourse studyList">
        <h2>The Complete JavaScript Course 2024: From Zero to Expert!</h2>
      </li>
    </ul>
  </div>
  <div class="projectsContainer">
    <a href="https://github.com/pati167/portfolio">
      <div class="projectPort projectComum">
        <img :src="githubImgPath" class="githubLogo" />
        <h3>Portfolio</h3>
      </div></a
    >
    <a href="https://github.com/pati167/game"
      ><div class="projectGame projectComum">
        <img :src="githubImgPath" class="githubLogo" />
        <h3>Game</h3>
      </div></a
    >
    <a href=""
      ><div class="projectBook projectComum">
        <img :src="githubImgPath" class="githubLogo" />
        <h3>Bookstrap</h3>
      </div></a
    >
    <a href="https://github.com/pati167/Luna-ToDo"
      ><div class="projectToDo projectComum">
        <img :src="githubImgPath" class="githubLogo" />
        <h3>Luna To-Do</h3>
      </div></a
    >
  </div>
  <div>
    <a class="gitLink" href="https://github.com/pati167">github.com/pati167</a>
  </div>
</template>

<style>
.studyContainer {
  position: absolute;
  left: 110px;
  top: 160px;
}
.studyTitle {
  padding-bottom: 30px;
  font-size: 40px;
  color: #8ca4bc;
}
.studyList {
  padding-bottom: 20px;
  color: #61788f;
  list-style: none;
}
.projectsContainer {
  position: absolute;
  left: 870px;
  top: 220px;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-gap: 10px;
  width: 300px;
  margin: 0 auto;
}
.projectComum {
  width: 250px;
  border: 2px solid #c0b8d1;
  border-radius: 10%;
  margin: 10px;
  padding: 50px;
  text-align: center;
  color: #8ca4bc;
  font-size: 20px;
  opacity: 70%;
}
.projectComum:hover {
  background-color: #c0b8d1;
  color: #61788f;
  opacity: 100%;
}
.githubLogo {
  width: 25px;
}

.gitLink {
  position: absolute;
  right: 100px;
  bottom: 100px;
  text-decoration: none;
  color: #b25068;
}
</style>

<script>
export default {
  data() {
    return {
      githubImgPath: "/github-logo.png",
    };
  },
};
</script>
