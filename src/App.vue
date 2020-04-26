<template>
  <div id="app">
    <!-- header -->
    
    <!-- content -->
    <div class="flex flex-col items-center justify-center">
      <p class="text-2xl">Deepak Bhardwaj</p>
      <social></social>
      <skills></skills>
      <div v-for="project in projects" :key="project.id">
        <a href="">
          <p :class="[project.status ? '' : 'line-through text-gray-300']">{{ project.title }}</p>
        </a>
      </div>
    </div>
    
    <!-- footer -->
    <div class="flex items-center justify-center">
      <p>Hosted on <i class="fab fa-github"></i></p>
    </div>
  </div>
</template>

<script>
import Social from "@/components/social";
import Skills from "@/components/skills";

export default {
  name: "app",
  data() {
    return {
      projects: [
        {
          id: 1,
          logo: "coheto",
          title: "CoHeTo",
          desc: "CoHeTo helps you go in presentation mode on Codepen and provides you some extra space to work with.",
          color: "green",
          shade: "500",
          icon: "fas fa-toggle-on",
          status: 1
        }, {
          id: 2,
          logo: "",
          title: "Contact App",
          desc: "CoHeTo helps you go in presentation mode on Codepen and provides you some extra space to work with.",
          color: "blue",
          shade: 500,
          icon: "far fa-id-badge",
          status: 1
        }, {
          id: 3,
          logo: "",
          title: "Giflib",
          desc: "CoHeTo helps you go in presentation mode on Codepen and provides you some extra space to work with.",
          color: "pink",
          shade: 500,
          icon: "fas fa-images",
          status: 0
        }, {
          id: 4,
          logo: "",
          title: "Timer",
          desc: "CoHeTo helps you go in presentation mode on Codepen and provides you some extra space to work with.",
          color: "indigo",
          shade: 500,
          icon: "fas fa-stopwatch",
          status: 1
        }, {
          id: 5,
          logo: "",
          title: "FlexBox Visualiser",
          desc: "CoHeTo helps you go in presentation mode on Codepen and provides you some extra space to work with.",
          color: "red",
          shade: 500,
          icon: "fab fa-buromobelexperte",
          status: 1
        }, {
          id: 6,
          logo: "",
          title: "Score keeper game",
          desc: "CoHeTo helps you go in presentation mode on Codepen and provides you some extra space to work with.",
          color: "orange",
          shade: 500,
          icon: "fas fa-dice",
          status: 1
        }, {
          id: 7,
          logo: "",
          title: "Color guessing game",
          desc: "CoHeTo helps you go in presentation mode on Codepen and provides you some extra space to work with.",
          color: "teal",
          shade: 500,
          icon: "fas fa-palette",
          status: 1
        }, {
          id: 8,
          logo: "",
          title: "Counter App",
          desc: "CoHeTo helps you go in presentation mode on Codepen and provides you some extra space to work with.",
          color: "orange",
          shade: 500,
          icon: "fas fa-stopwatch",
          status: 0
        }, {
          id: 9,
          logo: "",
          title: "Checkbox app | Subscription tracker",
          desc: "CoHeTo helps you go in presentation mode on Codepen and provides you some extra space to work with.",
          color: "blue",
          shade: 500,
          icon: "fas fa-check-double",
          status: 0
        }, {
          id: 10,
          logo: "",
          title: "81Hut",
          desc: "CoHeTo helps you go in presentation mode on Codepen and provides you some extra space to work with.",
          color: "pink",
          shade: 500,
          icon: "fas fa-home",
          status: 0
        }, {
          id: 11,
          logo: "",
          title: "Todo | using trello api",
          desc: "CoHeTo helps you go in presentation mode on Codepen and provides you some extra space to work with.",
          color: "red",
          shade: 500,
          icon: "fas fa-list-ol",
          status: 0
        }, {
          id: 12,
          logo: "",
          title: "Git client | Electron",
          desc: "CoHeTo helps you go in presentation mode on Codepen and provides you some extra space to work with.",
          color: "green",
          shade: 500,
          icon: "fas fa-code-branch",
          status: 0
        }, {
          id: 13,
          logo: "",
          title: "vidly app",
          desc: "CoHeTo helps you go in presentation mode on Codepen and provides you some extra space to work with.",
          color: "pink",
          shade: 500,
          icon: "fas fa-film",
          status: 0
        }, {
          id: 14,
          logo: "",
          title: "leave application chrome extension",
          desc: "CoHeTo helps you go in presentation mode on Codepen and provides you some extra space to work with.",
          color: "yellow",
          shade: 500,
          icon: "fas fa-trailer",
          status: 0
        }, {
          id: 15,
          logo: "",
          title: "DP Visualiser",
          desc: "CoHeTo helps you go in presentation mode on Codepen and provides you some extra space to work with.",
          color: "purple",
          shade: 500,
          icon: "fas fa-sitemap",
          status: 0
        }
      ]
    }
  },
  created() {},
  mounted() {},
  computed: {},
  watch: {},
  components: {
    Social,
    Skills
  }
};
</script>

<style>
* {
  padding: 0;
  margin: 0;
  outline: none;
  font-family: 'Nunito', sans-serif;
}
</style>