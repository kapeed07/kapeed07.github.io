<template>
  <div id="app">
    <div class="curved flex flex-col  justify-center items-center">
      <h2 class="text-3xl text-white">Deepak Bhardwaj</h2>
      <social></social>
    </div>
    <div class="flex flex-col h-full items-center justify-between">
      <div class="content m-10">
      <project-card v-for="project in projects" :project="project" :key="project.id"></project-card>

      </div>

      <div class="footer flex justify-center items-center text-white w-screen h-20">
        <p>
        Made with <i class="text-red-600 fas fa-heart"></i> in <span class="text-green-600 font-medium">VueJS </span>
        </p>
        <p class="pl-3">
        Hosted on <i class="text-white fab fa-github"></i>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
import ProjectCard from "@/components/project-card";
import Social from "@/components/social";
// import Skills from "@/components/skills";
// import DbHeader from "@/components/header";

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
          icon: "fas fa-toggle-on"
        }, {
          id: 2,
          logo: "",
          title: "Contact App",
          desc: "CoHeTo helps you go in presentation mode on Codepen and provides you some extra space to work with.",
          color: "blue",
          shade: 500,
          icon: "far fa-id-badge"
        }, {
          id: 3,
          logo: "",
          title: "Giflib",
          desc: "CoHeTo helps you go in presentation mode on Codepen and provides you some extra space to work with.",
          color: "pink",
          shade: 500,
          icon: "fas fa-images"
        }, {
          id: 4,
          logo: "",
          title: "Timer",
          desc: "CoHeTo helps you go in presentation mode on Codepen and provides you some extra space to work with.",
          color: "indigo",
          shade: 500,
          icon: "fas fa-stopwatch"
        }, {
          id: 5,
          logo: "",
          title: "FlexBox Visualiser",
          desc: "CoHeTo helps you go in presentation mode on Codepen and provides you some extra space to work with.",
          color: "red",
          shade: 500,
          icon: "fab fa-buromobelexperte"
        }, {
          id: 6,
          logo: "",
          title: "Score keeper game",
          desc: "CoHeTo helps you go in presentation mode on Codepen and provides you some extra space to work with.",
          color: "orange",
          shade: 500,
          icon: "fas fa-dice"
        }, {
          id: 7,
          logo: "",
          title: "Color guessing game",
          desc: "CoHeTo helps you go in presentation mode on Codepen and provides you some extra space to work with.",
          color: "teal",
          shade: 500,
          icon: "fas fa-palette"
        }, {
          id: 8,
          logo: "",
          title: "Counter App",
          desc: "CoHeTo helps you go in presentation mode on Codepen and provides you some extra space to work with.",
          color: "orange",
          shade: 500,
          icon: "fas fa-stopwatch"
        }, {
          id: 9,
          logo: "",
          title: "Checkbox app | Subscription tracker",
          desc: "CoHeTo helps you go in presentation mode on Codepen and provides you some extra space to work with.",
          color: "blue",
          shade: 500,
          icon: "fas fa-check-double"
        }, {
          id: 10,
          logo: "",
          title: "81Hut",
          desc: "CoHeTo helps you go in presentation mode on Codepen and provides you some extra space to work with.",
          color: "pink",
          shade: 500,
          icon: "fas fa-home"
        }, {
          id: 11,
          logo: "",
          title: "Todo | using trello api",
          desc: "CoHeTo helps you go in presentation mode on Codepen and provides you some extra space to work with.",
          color: "red",
          shade: 500,
          icon: "fas fa-list-ol"
        }, {
          id: 12,
          logo: "",
          title: "Git client | Electron",
          desc: "CoHeTo helps you go in presentation mode on Codepen and provides you some extra space to work with.",
          color: "green",
          shade: 500,
          icon: "fas fa-code-branch"
        }, {
          id: 13,
          logo: "",
          title: "vidly app",
          desc: "CoHeTo helps you go in presentation mode on Codepen and provides you some extra space to work with.",
          color: "pink",
          shade: 500,
          icon: "fas fa-film"
        }, {
          id: 14,
          logo: "",
          title: "leave application chrome extension",
          desc: "CoHeTo helps you go in presentation mode on Codepen and provides you some extra space to work with.",
          color: "yellow",
          shade: 500,
          icon: "fas fa-trailer"
        }, {
          id: 15,
          logo: "",
          title: "DP Visualiser",
          desc: "CoHeTo helps you go in presentation mode on Codepen and provides you some extra space to work with.",
          color: "purple",
          shade: 500,
          icon: "fas fa-sitemap"
        }
      ],
      searchTerm: ""
    }
  },
  computed: {
    // filteredProjects() {
    //   return this.projects.filter(project => project.title.toLowerCase().includes(this.searchTerm.toLowerCase()));
    // }
  },
  components: {
    ProjectCard,
    Social,
    // Skills,
    // DbHeader
  }
};
</script>

<style>

* {
  padding: 0;
  margin: 0;
}
.content {
  padding-top: 200px;
}
#app {
  height: 100%;
}
.db-text-black {
  color: #363537;
}
.curved {  
  position: fixed;
  width: 100%;
  z-index: 1;
  background: #DA3E52;
  /* filter: drop-shadow(2px 4px 1px #8cd867); */
  height: 200px;
  border-bottom-left-radius: 50% 30%;
  border-bottom-right-radius: 50% 30%;
}
.profile-image {
  filter: drop-shadow(4px 7px 5px #000);
}
.footer {
  background: #363537;
  /* position: absolute; */
  width: 100%;
  bottom: 0;
}

.box {

  border-left: 5px dashed #ef2d56;
  border-bottom: 5px dashed #ef2d56;
  
}

body {
  padding: 0;
  margin: 0;
  /* background-color: #ebf8ff; */
  font-family: 'Nunito', sans-serif;
}
/* #7034AC */
</style>
