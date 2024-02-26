<template>
  <div class="skillsContainer">
    <ul class="skillsInventory">
      <li
        v-for="(skill, index) in list"
        :key="index"
        @mouseover="showImage(skill)"
        class="skillsList"
      >
        {{ skill }}
      </li>
    </ul>
    <ul class="imageInventory">
      <li
        v-for="(image, index) in listImg"
        :key="index"
        :class="{
          imageList: true,
          show: selectedSkill === image.skill,
        }"
        :style="imageStyle(index, image.skill)"
      >
        <img :src="image.src" class="image" />
      </li>
    </ul>
  </div>
</template>

<style>
/* .skillsContainer {
  position: relative;
} */
.skillsInventory {
  list-style-type: none;
  position: absolute;
  right: 280px;
  bottom: 280px;
}
.skillsList {
  text-decoration: none;
  font-size: 50px;
  color: #8ca4bc;
  cursor: pointer;
  opacity: 50%;
}
.skillsList:hover {
  position: static;
  opacity: 100%;
  transition: opacity 1s ease;
  transition: font-size 1.5s ease;
  font-size: 51px;
}
.skillsList:not(:hover) {
  transition: font-size 1.5s ease;
}
.imageInventory {
  list-style-type: none;
  position: relative;
  right: 500px;
  bottom: 200px;
}

.imageList {
  overflow: hidden;
  position: absolute;
  transition: transform 1.5s ease;
}

.image {
  width: 400px;
}
</style>

<script>
export default {
  data() {
    return {
      list: ["Photography", "Drawing", "Editing", "Code"],
      listImg: [
        { skill: "Photography", src: "/public/skillsPhotography.jpeg" },
        { skill: "Drawing", src: "/public/skillsDrawing.jpeg" },
        { skill: "Editing", src: "/public/skillsEditing.jpeg" },
        { skill: "Code", src: "/public/skillsCode.jpeg" },
      ],

      selectedSkill: null,
    };
  },
  methods: {
    showImage(skill) {
      this.selectedSkill = skill;
    },
    imageStyle(index, skill) {
      let zIndex = this.listImg.length - index;
      if (this.selectedSkill === skill) {
        zIndex += this.listImg.length;
      }
      return {
        zIndex: zIndex,
        transform: this.selectedSkill === skill ? "scale(1.2)" : "scale(1)",
      };
    },
  },
};
</script>

skillStyle(skill){ this }
