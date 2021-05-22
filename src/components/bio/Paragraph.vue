<template>
  <div class="paragraph-container">
    <div class="title">
      <h2>{{ title }}</h2>
      <DetailButton @click="collapse = !collapse" />
    </div>
    <transition name="slide">
      <div class="detail" v-show="collapse">
        <slot></slot>
      </div>
    </transition>
  </div>
</template>

<script>
import DetailButton from "../DetailButton.vue";

export default {
  name: "Paragraph",
  components: { DetailButton },
  data() {
    return {
      collapse: this.initialCollapse,
    };
  },
  props: {
    title: String,
    initialCollapse: Boolean,
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

.title {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}

.detail {
  overflow: hidden;
  max-height: 100%;
}

.slide-enter-active,
.slide-leave-active {
  transition: height 0.5s ease-in-out;
}

.slide-enter-from,
.slide-leave-to {
  height: 0%;
}

.slide-enter-to,
.slide-leave-from {
  height: 100%;
}
</style>