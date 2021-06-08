<template>
  <a class="item" :href="itemId">
    <span class="material-icons material-icons-outlined"> {{ icon }} </span>
    <span class="title">{{ title }}</span></a
  >
</template>

<script>
export default {
  name: "Item",
  props: {
    itemId: String,
    title: String,
    icon: String,
  },
};
</script>

<style scoped>
.item {
  padding: 1rem;
  text-decoration: none;
  display: flex;
  align-items: center;
  color: white;
}

.title {
  margin-left: 0.5rem;
  text-transform: uppercase;
  font-weight: 600;
}
</style>