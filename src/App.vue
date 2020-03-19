<template>
  <div id="app">
    <div class="container px-3">
      <db-header></db-header>
      <!-- <skills></skills>
      <social></social> -->
      <input
        class="shadow-md my-4 p-2 pl-6 w-full outline-none rounded-lg"
        type="text"
        placeholder="Search"
        autofocus
        v-model="searchTerm"
      />
      <div class="flex flex-wrap">
        <project-card
          v-for="project in filteredProjects"
          :key="project.id"
          :project="project"
        ></project-card>
      </div>
    </div>
  </div>
</template>

<script>
import ProjectCard from "@/components/project-card";
// import Social from "@/components/social";
// import Skills from "@/components/skills";
import DbHeader from "@/components/header";

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
    filteredProjects() {
      return this.projects.filter(project => project.title.toLowerCase().includes(this.searchTerm.toLowerCase()));
    }
  },
  components: {
    ProjectCard,
    // Social,
    // Skills,
    DbHeader
  }
};
</script>

<style>
body {
  background-color: #ebf8ff;
  font-family: 'Nunito', sans-serif;
}
/* #7034AC */
</style>
