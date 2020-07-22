<template>
  <div class="flex w-40 items-center flex-wrap">
    <a v-for="social in socials" :key="social._id" :href="social.url" target="blank">
      <i
        v-if="social.url"
        class="text-2xl text-gray-800 cursor-pointer m-2"
        :class="`${social.icon} ${social.url ? '' : 'text-gray-300'}`"
      ></i>
    </a>
  </div>
</template>

<script>
import socials from "../constants/socials";

export default {
  name: "Social",
  data() {
    return {
      socials,
    };
  },
};
</script>