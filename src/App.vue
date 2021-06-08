<template>
  <div class="sidebar-container">
    <div class="photo"><img src="./assets/me.png" /></div>
    <div class="items-container">
      <Item
        v-for="item in items"
        :title="item.title"
        :itemId="item.id"
        :icon="item.icon"
        :key="item.id"
      />
    </div>
  </div>
</template>

<script>
import Item from "./components/Item";
import { menuItems } from "./menu";
export default {
  name: "App",
  components: {
    Item,
  },
  data: () => {
    return {
      items: menuItems,
    };
  },
};
</script>

<style scoped>
.sidebar-container {
  position: relative;
  width: 100%;
  padding-top: 1rem;
  background: #42b983;
  height: 100%;
  overflow: hidden;
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

.items-container {
  margin-top: 2rem;
  overflow: auto;
}
</style>
