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

p {
  display: block;
  width: 400px;
  font-size: 16px;
  font-weight: bold;
  font-family: "akayla Personal Use Only", sans-serif;
  letter-spacing: 1.2px;
}

p::before, p::after {
  background-color: #22bb66;
  content: "";
  display: inline-block;
  height: 1px;
  position: relative;
  vertical-align: middle;
  width: 25%;
}

p::before {
  right: 1em;
}

p::after {
  left: 1em;
}
</style>