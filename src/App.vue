<template>
  <Navbar />
  <div class="main">
    <Landing />
    <Bio />
  </div>
</template>

<script>
import Navbar from "./components/navbar/Navbar.vue";
import Landing from "./components/Landing.vue";
import Bio from "./components/bio/Bio.vue";

export default {
  name: "App",
  components: {
    Navbar,
    Landing,
    Bio,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;700&display=swap");

body {
  margin: 0;
  padding: 0;
}

#app {
  font-family: "Montserrat", Avenir, Helvetica, Arial, sans-serif;
  font-size: 16px;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  box-sizing: border-box;
  margin-right: 0;
  margin-left: 0;
}

.main {
  margin-top: 50px;
}
</style>
