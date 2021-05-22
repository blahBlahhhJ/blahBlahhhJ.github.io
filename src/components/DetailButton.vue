<template>
  <button class="detail-btn">
    <span class="dot"></span>
    <span class="dot"></span>
    <span class="dot"></span>
  </button>
</template>

<script>
export default {
  name: "DetailButton",
};
</script>

<style scoped>
.detail-btn {
  background-color: #2c3e50;
  border: 1px solid #2c3e50;
  border-radius: 2rem;
  padding: 0.7rem 0.5rem;
  display: flex;
  flex-direction: row;
  align-items: center;
}

.dot {
  height: 0.4rem;
  width: 0.4rem;
  margin: 0 0.2rem;
  background-color: white;
  border-radius: 0.4rem;
}
</style>