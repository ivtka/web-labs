<template>
  <div class="block-date">{{ date }}</div>
</template>

<script>
export default {
  name: "BlockDate",
  props: {
    date: String,
  },
};
</script>

<style>
.block-date {
  text-transform: uppercase;
  font-family: var(--page-font);
  color: #838383;
  font-weight: 400;
  font-size: 12px;
  letter-spacing: 1.8px;
  display: flex;
  justify-content: center;
  align-items: center;
  border: 1px solid #dfdfdf;
  height: 29px;
  width: 142px;
}
</style>