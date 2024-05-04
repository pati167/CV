<template>
  <div class="searchContainer">
    <ul class="searchList">
      <li class="searchExperience">
        <a @click="scrollToExperience">Experience</a>
      </li>
      <li class="searchEducation">
        <a @click="scrollToEducation">Education</a>
      </li>
    </ul>
  </div>

  <div class="mainContainer">
    <div class="projectContainer" ref="projectContainer">
      <div class="projectGrid">
        <a
          v-for="(project, index) in projects"
          :key="index"
          :href="project.link"
          class="projectLink"
        >
          <div class="projectColumn">
            <img :src="iconSvg" class="githubIcon" />
            <h1 class="projectTitle">{{ project.title }}</h1>
            <p class="projectDescription">{{ project.description }}</p>
          </div>
        </a>
      </div>
    </div>
    <div class="educationContainer" ref="educationContainer">
      <h1 class="educationTitle">Education</h1>
      <ul class="educationList">
        <li class="educationColumn">
          <span class="bold">The complete Web Development Bootcamp</span> <br />
          Dr. Angela Yu
        </li>
        <li class="educationColumn">
          <span class="bold"
            >The complete JavaScript Course from Zero to Hero
          </span>
          <br />
          Jonas Schmedtmann
        </li>
        <li class="educationColumn">
          <span class="bold">English course</span> <br />
          Skills Gym, Cambridge University Press Learning Partner
        </li>
        <li class="educationColumn">
          <span class="bold">Communication and AudioVisual</span> <br />
          António Arroio School of Arts
        </li>
      </ul>
    </div>
  </div>
</template>

<style>
.searchList {
  position: fixed;
  top: 200px;
  left: 20px;
  color: #27374d;
  text-decoration: none;
  list-style: none;
  font-size: 20px;
}
.searchList :hover {
  font-weight: 700;
}
.leader {
  width: 500px;
  height: 200px;
}

.mainContainer {
  position: absolute;
  right: 100px;
  top: 200px;
}
.projectContainer {
  margin-bottom: 100px;
  margin-left: 120px;
}
.projectGrid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
}

.projectLink {
  text-decoration: none;
  color: inherit;
}

.projectColumn {
  padding: 20px;
  background-color: #526d82;
  border-top-right-radius: 20px;
  height: 280px;
  width: 388px;
  z-index: 2;
}
.githubIcon {
  width: 45px;
  height: 45px;
}
.projectTitle {
  font-size: 22px;
  color: #f6f1f1;
  margin: 30px 0 10px 0;
  font-family: "Merriweather", serif;
  font-weight: 700;
  font-style: normal;
}
.projectDescription {
  font-size: 18px;
  color: #f6f1f1;
}

.educationContainer {
  background-color: #526d82;
  width: 100%;
  margin-bottom: 100px;
  padding: 80px 150px 80px 200px;
  color: #f6f1f1;
}
.educationList {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
  list-style-type: none;
  padding: 0;
}
.educationColumn {
  margin: 10px 20px 0 0;
  font-size: 16px;
}
.educationTitle {
  font-family: "Merriweather", serif;
  font-weight: 700;
  font-style: normal;
  font-size: 35px;
}
.bold {
  font-weight: 700;
}
</style>

<script>
export default {
  data() {
    return {
      iconSvg: "./public/githubIcon.png",

      projects: [
        {
          title: "Photography Portfolio",
          description:
            "Create a web-portfolio using HTML, CSS, and JavaScript.",
          link: "https://github.com/pati167/portfolio",
        },
        {
          title: "Login",
          description: "Created a login page with HTML and CSS.",
          link: "https://github.com/pati167/Login",
        },
        {
          title: "Dating App",
          description: "Created a page for a dating site using Bootstrap.",
          link: "https://github.com/pati167/Dating-web",
        },
        {
          title: "Game",
          description: "Game built using HTML, CSS, and JavaScript.",
          link: "https://github.com/pati167/game",
        },
        {
          title: "Luna To-Do",
          description: "Built a To-Do list application with Quasar.",
          link: "https://github.com/pati167/Luna-ToDo",
        },
        {
          title: "Celiac app - In progress",
          description:
            "Create a search engine that finds products from a backend API.",
          link: "https://www.figma.com/file/qE6QljauVmEBh3Hjl795NV/Celiac?type=design&node-id=0-1&mode=design&t=QyYdBc6RX6euFrcO-0",
        },
      ],
    };
  },
  methods: {
    scrollToExperience() {
      this.$refs.projectContainer.scrollIntoView({ behavior: "smooth" });
    },
    scrollToEducation() {
      this.$refs.educationContainer.scrollIntoView({ behavior: "smooth" });
    },
  },
};
</script>
