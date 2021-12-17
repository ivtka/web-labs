<template>
  <div class="post">
    <img v-bind:src="picture_source" />
    <div class="info">
      <div class="tag-wrapper">
        <div class="tags">
          <Tag v-for="(tag, index) in tags" :key="index" :tag="tag" id="tag" />
        </div>
      </div>
      <div class="post-title">{{ post_title }}</div>
      <div class="post-text">{{ post_text }}</div>
      <Bottom />
    </div>
  </div>
</template>

<script>
import Tag from "./post/Tag.vue";
import Bottom from "./post/Bottom.vue";

export default {
  name: "Post",
  props: {
    picture_source: String,
    tags: Array,
    post_title: String,
    post_text: String,
  },
  components: {
    Tag,
    Bottom,
  },
};
</script>

<style>
.post {
  width: 768px;
  height: 768px;
}

.info {
  height: 48.5%;
  margin-top: -5px;
}

.tag-wrapper {
  width: 100%;
  display: flex;
  justify-content: center;
}

.tags {
  display: flex;
  margin-top: 30px;
}

#tag:not(:last-child)::after {
  content: "";
  border-radius: 50%;
  display: inline-block;
  width: 5px;
  height: 5px;
  background-color: #c7c7c7;
  position: relative;
  right: -12px;
  top: 10px;
}

.post-title {
  font-family: var(--page-font);
  font-weight: 700;
  font-size: 20px;
  color: #262626;
  margin: 35px auto 40px auto;
  width: 610px;
}

.post-text {
  font-family: "Droid Serif";
  font-weight: 400;
  font-size: 13px;
  width: 600px;
  margin: 0 auto;
  line-height: 24px;
  color: #4a4a4a;
}
</style>