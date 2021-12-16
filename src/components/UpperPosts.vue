<template>
  <div class="upper-posts">
    <BrokenShape />
    <Shape v-for="i in 2" :key="i" />
  </div>
</template>

<script>
import Shape from "./upper-posts/Shape.vue";
import BrokenShape from "./upper-posts/BrokenShape.vue";

export default {
  name: "UpperPosts",
  components: {
    Shape,
    BrokenShape,
  },
};
</script>

<style>
.upper-posts {
  margin-top: 85px;
  display: flex;
  justify-content: space-around;
}
</style>