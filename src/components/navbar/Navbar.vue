<template>
  <div class="navbar">
    <div class="title">
      <img alt="Vue Logo" src="../../assets/logo.png" />
      <a href="#">Jason S. Wang</a>
    </div>
    <div class="nav-items">
      <Navitem
        v-for="nav in navs"
        :key="nav.key"
        :title="nav.title"
        :link="nav.link"
        :extern="nav.extern"
        :droppable="nav.droppable"
      />
    </div>
  </div>
</template>

<script>
import Navitem from "./Navitem.vue";

export default {
  name: "Navbar",
  components: {
    Navitem,
  },
  data() {
    return {
      navs: [
        {
          key: 0,
          title: "Home",
          link: "#",
          extern: false,
          droppable: false,
        },
        {
          key: 1,
          title: "Projects",
          link: "#",
          extern: false,
          droppable: false,
        },
        {
          key: 2,
          title: "Music",
          link: "#",
          extern: false,
          droppable: false,
        },
        {
          key: 3,
          title: "GitHub",
          link: "https://github.com/blahBlahhhJ",
          extern: true,
          droppable: false,
        },
        {
          key: 4,
          title: "LinkedIn",
          link: "https://www.linkedin.com/in/jason-wang-468117193/",
          extern: true,
          droppable: false,
        },
      ],
    };
  },
};
</script>

<style scoped>
.navbar {
  display: flex;
  flex-direction: row;
  align-items: center;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 40px;
  padding: 5px 10px;
  border-bottom: 1px solid #6185a8;
  z-index: 20;
  background-color: white;
}

.title {
  height: 100%;
  display: flex;
  flex-direction: row;
  align-items: center;
  flex: 1.5;
}

.title > a {
  font-size: 1.6rem;
  color: #2c3e50;
  text-decoration: none;
  font-weight: 700;
}

.title > img {
  height: 50%;
  margin-right: 1rem;
}

.nav-items {
  display: flex;
  flex-direction: row;
  align-items: center;
  flex: 1;
  height: 100%;
}
</style>