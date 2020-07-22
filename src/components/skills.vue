<template>
  <div>
    <i v-for="skill in skills" :key="skill._id" :class="`text-2xl text-gray-700 m-2 ${skill.icon}`"></i>
  </div>
</template>

<script>
import skills from "../constants/skills";

export default {
  name: "Skills",
  data() {
    return {
      skills,
    };
  },
};
</script>