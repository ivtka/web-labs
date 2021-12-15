<template>
  <div class="top">
    <Menu />
    <SocialMedia />
    <Tagline />
    <Logo />
    <Slider />
  </div>
</template>


<script>
import Menu from "./top/Menu.vue";
import SocialMedia from "./top/SocialMedia.vue";
import Tagline from "./top/Tagline.vue";
import Logo from "./top/Logo.vue";
import Slider from "./top/Slider.vue";

export default {
  name: "Top",
  components: {
    Menu,
    SocialMedia,
    Tagline,
    Logo,
    Slider,
  },
};
</script>
