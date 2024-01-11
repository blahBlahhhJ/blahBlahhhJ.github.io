<template>
  <div class="project-container">
    <div class="title">
      <span>{{ date }}</span>
      <h3>{{ title }}</h3>
    </div>
    <div class="discription">
      <img alt="project image" :src="imageSrc" />
      <div class="text">
        <slot></slot>
        <a class="gh-btn btn" :class="repoClass" :href="repo"
          >View GitHub Repo / Code</a
        >
        <a class="website-btn btn" :class="siteClass" :href="site"
          >View Project Website / Report</a
        >
      </div>
    </div>
  </div>
  <hr />
</template>

<script>
export default {
  name: "Project",
  data() {
    return {
      repoClass: this.btnClass(this.repo),
      siteClass: this.btnClass(this.site),
    };
  },
  props: {
    image: String,
    date: String,
    title: String,
    repo: String,
    site: String,
  },
  computed: {
    imageSrc() {
      return require("@/assets/project/" + this.image);
    },
  },
  methods: {
    btnClass(link) {
      return link == null ? "btn-inactive" : "btn-active";
    },
  },
};
</script>

<style scoped>
.project-container {
  margin: 2rem 0;
}

.title {
  display: flex;
  flex-direction: row;
  margin-bottom: 1rem;
}
.title > span {
  flex: 1;
  margin-right: 2rem;
}
.title > h3 {
  flex: 3;
  margin: 0;
}

.discription {
  display: flex;
  flex-direction: row;
  align-items: center;
}
.discription > img {
  flex: 1;
  margin-right: 2rem;
  width: 0;
  border-radius: 1rem;
}
.discription > .text {
  flex: 3;
}

.btn {
  display: inline-block;
  text-decoration: none;
  font-weight: 600;
  color: #2c3e50;
  border: 1px solid #2c3e50;
  border-radius: 0.7rem;
  margin-top: 1rem;
  margin-right: 2rem;
  padding: 0.7rem;

  transition: color, background-color 0.3s ease;
}

.btn-inactive {
  color: #8d9aa8;
  border-color: #8d9aa8;
  text-decoration: line-through;
}

.btn-active:hover {
  transition: all 0.3s ease-out;
  color: white;
  background-color: #2c3e50;
}
</style>