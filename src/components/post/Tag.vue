<template>
  <div id="tag">
    <span class="tag">{{ tag }}</span>
  </div>
</template>

<script>
export default {
  name: "Tag",
  props: {
    tag: String,
  },
};
</script>

<style>
#tag {
  border: 1px solid #22bb66;
  width: 80px;
  height: 25px;
  margin-right: 18px;
  font-family: var(--page-font);
  font-size: 10px;
  color: #22bb66;
  font-weight: bold;
  letter-spacing: 1.8px;
  text-transform: uppercase;
  display: flex;
  border-radius: 5px;
}

.tag {
  margin: auto;
  position: relative;
}
</style>