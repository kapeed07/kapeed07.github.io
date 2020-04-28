<template>
  <div id="app">
    <!-- header -->
    
    <!-- content -->
    <div class="flex flex-col items-center justify-center">
      <p class="text-2xl">Deepak Bhardwaj</p>
      <social></social>
      <skills></skills>
      <div v-for="project in projects" :key="project.id">
        <div class="flex items-center" :class="[project.status ? '' : 'line-through text-gray-300']">
          <img
            v-if="project.logo"
            :src="getLogoUrl(project.logo)"
            class="w-5"
            :alt="project.logo">
          <i v-else :class="project.icon"></i>
          <p class="ml-2">{{ project.title }}</p>
        </div>
      </div>
      <p class="codepen" data-height="500" data-theme-id="dark" data-default-tab="result" data-user="kapeed07" data-slug-hash="OJygBgK" style="height: 161px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="OJygBgK">
  <span>See the Pen <a href="https://codepen.io/kapeed07/pen/OJygBgK">
  OJygBgK</a> by Deepak Bhardwaj  (<a href="https://codepen.io/kapeed07">@kapeed07</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

<p class="codepen" data-height="500" data-theme-id="dark" data-default-tab="result" data-user="kapeed07" data-slug-hash="ZEbyRgr" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="_profile-image-rotate">
  <span>See the Pen <a href="https://codepen.io/kapeed07/pen/ZEbyRgr">
  _profile-image-rotate</a> by Deepak Bhardwaj  (<a href="https://codepen.io/kapeed07">@kapeed07</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>


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
  methods: {
    getLogoUrl(logo) {
      return require(`@/assets/img/${logo}.png`);
    }
  },
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