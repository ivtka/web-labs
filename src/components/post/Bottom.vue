<template>
  <div class="bottom-tags">
    <BlockDate :date="`April 29, 2014`" />
    <SocialMedia />
    <div class="button-read-more">
      <button class="read-more">Read More</button>
      <button class="btn-next">&#10095;</button>
    </div>
  </div>
</template>

<script>
import SocialMedia from "./SocialMedia.vue";
import BlockDate from "./BlockDate.vue";

export default {
  name: "Bottom",
  components: {
    SocialMedia,
    BlockDate,
  },
};
</script>

<style>
.bottom-tags {
  width: 600px;
  display: flex;
  justify-content: space-between;
  margin: 45px auto 0 auto;
}

.button-read-more button.read-more {
  width: 140px;
  height: 29px;
  border: 1px solid #dfdfdf;
  background-color: #ffffff;
  color: #838383;
  font-family: var(--page-font);
  font-weight: 400;
  text-transform: uppercase;
}

.button-read-more button.btn-next {
  display: inline-block;
  cursor: pointer;
  color: white;
  text-align: center;
  background-color: #22bb66;
  width: 25px;
  height: 29px;
  border: none;
}
</style>
