<template>
  <div class="posts">
    <div></div>
    <div>
      <Post
        v-for="i in 5"
        :key="i"
        :picture_source="require('../../public/img.png')"
        :tags="[`travel`, `travel`]"
        style="margin-bottom: 70px"
        :post_title="`Playfair Display: A new level of new typefaces and fonts
that will make you literally glow...`"
        :post_text="`Ready to amp up your closet with the season's must-have accessory? Thanks to celebs like Kendall Jenner and Rosie Huntington-Whiteley, Western-inspired belts have quickly become fashion’s cool-girl accessory. Really, we’ve gathered a gang of stylish celebs and top bloggers wearing the big-buckled belt to prove the accessory amps up any outfit. So, are you ready.`"
      />
    </div>
  </div>
</template>

<script>
import Post from "./Post.vue";

export default {
  name: "Posts",
  components: {
    Post,
  },
};
</script>


<style>
.posts {
  margin-top: 70px;
  display: grid;
  grid-template-columns: 1fr 1fr;
}
</style>