<template>
  <div class="social">
    <a target="_blank" href="https://github.com/vmwatanabe"><GitHub /></a>
    <a
      target="_blank"
      href="https://www.linkedin.com/in/victor-matos-watanabe-0b2119b4/"
      ><LinkedIn
    /></a>
  </div>
</template>

<script>
import GitHub from "../CustomIcons/GitHub";
import LinkedIn from "../CustomIcons/LinkedIn";

export default {
  name: "SocialLinks",
  components: { GitHub, LinkedIn },
};
</script>

<style scoped>
.social {
  margin-top: 1rem;
}
.social > a {
  cursor: pointer;
}
.social > a > svg {
  fill: white;
}
.social > a:not(:first-child) {
  margin-left: 0.5rem;
}
</style>