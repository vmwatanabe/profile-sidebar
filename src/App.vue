<template>
  <div class="sidebar-container">
    <div class="photo-container">
      <div class="photo"><img src="./assets/me.png" /></div>
      <div class="photo-title">Watanabe, The Dev</div>
      <SocialLinks />
    </div>
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
import SocialLinks from "./components/SocialLinks";
import { menuItems } from "./menu";

export default {
  name: "App",
  components: {
    Item,
    SocialLinks,
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
  color: white;
}

.photo-container {
  display: flex;
  align-items: center;
  flex-direction: column;
}

.photo-title {
  margin-top: 1rem;
  font-weight: 600;
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
  margin-top: 1rem;
  overflow: auto;
}
</style>
