<template>
  <div class="navitem">
    <a :href="link">{{ title }}</a>
    <div class="dot"></div>
  </div>
</template>

<script>
export default {
  name: "Navitem",
  props: {
    title: String,
    link: String,
    extern: Boolean,
    droppable: Boolean,
  },
};
</script>

<style scoped>
.navitem {
  display: flex;
  flex-direction: row;
  align-items: center;
  margin-right: 1rem;
}

a {
  color: #486685;
  margin-right: 1rem;
  text-decoration: none;
  font-weight: 600;
}

a:hover {
  color: #2c3e50;
}

.dot {
  height: 2px;
  width: 2px;
  background: black;
}
</style>