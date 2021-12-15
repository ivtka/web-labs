<template>
  <div class="slideshow">
    <div class="slide" v-for="index in 10" :key="index">
      <div class="head">
        {{index}} Playfair Display: A new generation of typefaces and fonts.
      </div>
      <div class="text">
        Coming from two different cultures has been instrumental in<br />
        how we've approached our design process. Himmelen is a daily updated
        everyday moments from all over the world.
      </div>
      <div class="button">
        <button>Read more</button>
      </div>
    </div>

    <a class="prev" v-on:click="this.nextSlide(-1)">&#10094;</a>
    <a class="next" v-on:click="this.nextSlide(1)">&#10095;</a>
  </div>
</template>

<script>
export default {
  setup() {},
  data() {
    return {
      slide_index: 1,
    };
  },
  methods: {
    showSlide: function (index) {
      let slides = document.getElementsByClassName("slide");
      if (index > slides.length) {
        this.slide_index = 1;
      }
      if (index < 1) {
        this.slide_index = slides.length;
      }

      for (let i = 0; i < slides.length; i++) {
        slides[i].style.display = "none";
      }
      slides[this.slide_index - 1].style.display = "flex";
    },
    nextSlide: function (n) {
      this.showSlide((this.slide_index += n));
    },
  },
};
</script>

<style>
* {
  box-sizing: border-box;
}

.slideshow {
  font-family: var(--page-font);
  font-weight: 700;
  max-width: 100vw;
  min-height: 600px;
  position: relative;
  margin: auto;
  background-color: rgba(0, 0, 0, 0.6);
}

.prev,
.next {
  cursor: pointer;
  position: absolute;
  top: 50%;
  width: auto;
  margin-top: -22px;
  margin-left: 120px;
  padding: 14.5px;
  color: white;
  font-weight: bold;
  font-size: 15px;
  user-select: none;
  background-color: rgba(0, 0, 0, 0.4);
}

.prev:hover,
.next:hover {
  background-color: rgba(0, 0, 0, 0.6);
}

.next {
  right: 0;
  margin-right: 120px;
}

.slide {
  width: 500px;
  height: 570px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  color: #ffffff;
}

.slide .head {
  line-height: 38px;
  font-size: 25px;
  margin-bottom: 40px;
}

.slide .text {
  line-height: 24px;
  font-family: "Droid Serif", sans-serif;
  font-size: 15px;
  font-style: italic;
  margin-bottom: 50px;
}

.slide .button {
  background-color: #ffffff2f;
  width: 181px;
  height: 56px;
  padding: 7px;
}

.slide button {
  font-weight: 700;
  text-transform: uppercase;
  font-size: 13px;
  color: #ffffff;
  border: none;
  height: 42px;
  width: 167px;
  box-shadow: 0 2px 1px rgba(11, 145, 70, 0.35);
  background-color: #22bb66;
}

.slide button:hover,
button:focus {
  cursor: pointer;
}

.slide:nth-child(n + 2) {
  display: none;
}

.slide:nth-child(2n) {
  color: #000000;
}

.slide:nth-child(3n) {
  color: #4d4d4d;
}
</style>