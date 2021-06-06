<template>
  <div class="sidebar-container">
    <div class="photo"><img src="./assets/me.png" /></div>

    <div class="items-container">
      <Item
        v-for="item in items"
        :title="item.title"
        :itemId="item.id"
        :key="item.id"
      />
    </div>
  </div>
</template>

<script>
import Item from "./components/Item";

const items = [
  {
    id: "home",
    title: "Home",
  },
];

export default {
  name: "App",
  components: {
    Item,
  },
  data: () => {
    return {
      items,
    };
  },
};
</script>

<style scoped>
.sidebar-container {
  position: relative;
  width: 100%;
  padding-top: 1rem;
}

.photo {
  width: 80%;
  border-radius: 33vw;
  overflow: hidden;
  margin: auto;
}

img {
  width: 100%;
}
</style>
