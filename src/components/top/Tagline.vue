<template>
  <div class="tagline">
    <p>your tagline will go right here</p>
  </div>
</template>

<style>
.tagline {
  margin-top: 30px;
  display: flex;
  justify-content: center;
}

.tagline p {
  display: block;
  width: 400px;
  font-size: 16px;
  font-weight: bold;
  font-family: "akayla Personal Use Only", sans-serif;
  letter-spacing: 1.2px;
}

.tagline p::before, .tagline p::after {
  background-color: #22bb66;
  content: "";
  display: inline-block;
  height: 1px;
  position: relative;
  vertical-align: middle;
  width: 25%;
}

.tagline p::before {
  right: 1em;
}

.tagline p::after {
  left: 1em;
}
</style>