<template>
  <div class="project-container">
    <div class="title">
      <span>{{ date }}</span>
      <img alt="project image" :src="imageSrc" />
    </div>
    <div class="discription">
      <h3>{{ title }}</h3>
      <slot></slot>
      <a class="gh-btn btn" :class="repoClass" :href="repo">View GitHub Repo</a>
      <a class="website-btn btn" :class="siteClass" :href="site"
        >View Project Website</a
      >
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
  display: flex;
  flex-direction: row;
  align-items: top;
  margin: 2rem 0;
}

.project-container > .title {
  flex: 1;
  margin-right: 2rem;
  text-align: center;
}

.project-container > .title > img {
  width: 100%;
  border-radius: 1rem;
  margin-top: 1rem;
}

.project-container > .title > span {
  padding: 0.5rem;
}

.project-container > .discription {
  flex: 3;
}

h3 {
  margin-top: 0;
  margin-bottom: 1rem;
}

.btn {
  display: inline-block;
  text-decoration: none;
  font-weight: 600;
  color: #2c3e50;
  border: 1px solid #2c3e50;
  border-radius: 0.5rem;
  margin-top: 1rem;
  margin-right: 2rem;
  padding: 0.7rem;
}

.btn-inactive {
  color: #8d9aa8;
  border-color: #8d9aa8;
  text-decoration: line-through;
}

.btn-active:hover {
  transition: all 0.5s ease-out;
  color: white;
  background-color: #2c3e50;
}
</style>