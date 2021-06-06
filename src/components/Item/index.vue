<template>
  <a class="item" :href="itemId">{{ title }}</a>
</template>

<script>
export default {
  name: "Item",
  props: {
    itemId: String,
    title: String,
  },
};
</script>

<style scoped>
.item {
  padding: 1rem;
}
</style>