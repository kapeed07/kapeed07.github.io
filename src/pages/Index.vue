<template>
  <div class="flex flex-col items-center justify-center">
    <Header />
    <Social />
    <Skills />
    <Projects />
  </div>
</template>

<script>
import Social from "@/components/Social";
import Header from "@/components/Header";
import Skills from "@/components/Skills";
import Projects from "@/components/Projects";

export default {
  name: "Index",
  data() {
    return {};
  },
  created() {},
  mounted() {},
  computed: {},
  watch: {},
  methods: {},
  components: {
    Social,
    Skills,
    Header,
    Projects,
  },
};
</script>