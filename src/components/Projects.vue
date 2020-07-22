<template>
  <div>
    <template v-for="project in projects">
      <div
        v-if="project.status"
        :key="project._id"
        class="bg-white p-5 border border-gray-400 m-2 rounded-md opacity-100"
        :class="[project.status ? '' : 'line-through text-gray-300']"
      >
        <a :href="project.url" class="flex items-center" target="blank">
          <img
            v-if="project.logo"
            :src="getImageUrl(project.logo, 'png')"
            class="w-5"
            :alt="project.logo"
          />
          <i v-else :class="project.icon"></i>
          <p class="ml-2">{{ project.title }}</p>
          <p class="ml-2">{{ project.desc }}</p>
        </a>
      </div>
    </template>
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