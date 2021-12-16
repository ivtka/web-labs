<template>
  <Top />
  <UpperPosts />
  <Posts />
</template>

<script>
import Top from "./components/Top.vue";
import UpperPosts from "./components/UpperPosts.vue";
import Posts from "./components/Posts.vue";

export default {
  name: "App",
  components: {
    Top,
    UpperPosts,
    Posts,
  },
};
</script>

<style>
* {
  list-style: none;
  text-decoration: none;
  padding: 0;
  margin: 0;
}

:root {
  --page-font: "Montserrat", sans-serif;
}
</style>
