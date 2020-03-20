<template>
  <div class="w-full sm:w-1/2 sm:px-1 md:p-3 md:w-1/3">
    <div
      :class="`mb-4 shadow-lg hover:shadow-2xl rounded-md bg-${project.color}-${project.shade} p-6`"
    >
      <div class="flex-col">
        <div class="flex items-center">
          
          
          <div
            class="db-logo flex items-center justify-center mr-6  rounded-full"
            :class="[project.logo ? '' : `border border-${project.color}-${project.shade + 100} bg-${project.color}-${project.shade - 100}`]">
          <img
            v-if="project.logo"
            :src="getLogoUrl"
            alt=""
          />

          <i v-else :class="`text-2xl text-gray-100 ${project.icon}`"></i>

          </div>
            
          <p class="capitalize text-white font-semibold text-4xl sm:text-2xl md:text-2xl">
            {{project.title}}
          </p>
        </div>
        <p class="text-white mt-6 tracking-wider">
          {{project.desc}}
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "project-card",
  props: ["project"],
  computed: {
    getLogoUrl() {
      return require(`@/assets/img/${this.project.logo}.png`);
    }
  }
};
</script>
<style  scoped>
.db-logo {
  min-width: 5rem;
  min-height: 5rem;
  max-width: 5rem;
  max-height: 5rem;
}
</style>