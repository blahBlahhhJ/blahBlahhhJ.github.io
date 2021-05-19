<template>
  <div class="paragraph-container">
    <h2>{{ title }}</h2>
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "Paragraph",
  props: {
    title: String,
  },
};
</script>

<style scoped>
.paragraph-container {
  text-align: left;
}

h2 {
  margin: 0;
}
</style>