<template>
  <div class="flex justify-center items-center w-full mt-20 mb-10">
    <img class="logo rounded-full mr-5" :src="getImageUrl('kapeed07', 'jpg')" />
    <p class="text-2xl">Deepak Bhardwaj</p>
  </div>
</template>

<script>
import getImageUrl from "@/utils";

export default {
  name: "Header",
  data() {
    return {};
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

<style scoped>
.logo {
  width: 30px;
  height: 30px;
}
</style>