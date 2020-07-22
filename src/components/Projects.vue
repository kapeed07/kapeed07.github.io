<template>
  <div>
    <div
      v-for="project in projects"
      :key="project._id"
      class="flex items-center p-5 border border-gray-300 m-2 rounded-md"
      :class="[project.status ? '' : 'line-through text-gray-300']"
    >
      <img
        v-if="project.logo"
        :src="getImageUrl(project.logo, 'png')"
        class="w-5"
        :alt="project.logo"
      />
      <i v-else :class="project.icon"></i>
      <p class="ml-2">{{ project.title }}</p>
    </div>
  </div>
</template>

<script>
import projects from "@/constants/projects";
import getImageUrl from "@/utils";

export default {
  name: "Projects",
  data() {
    return {
      projects,
    };
  },
  created() {},
  mounted() {},
  computed: {},
  watch: {},
  methods: {
    getImageUrl,
  },
  components: {},
};
</script>