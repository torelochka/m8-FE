<template>
  <div class="container" :style="{ width: width + 'px' }">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "Container",
  props: {
    width: {
      type: Number,
      default: 200,
    },
  },
};
</script>

<style scoped>
.container {
  margin: 0 auto;
  min-height: calc(93vh - 120px);
  width: 200px;
  padding: 30px 0 70px;
}

@media (max-width: 320px) {
  .container {
    width: 280px !important;
  }
}
</style>
