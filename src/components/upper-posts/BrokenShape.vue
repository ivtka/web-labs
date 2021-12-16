<template>
  <div class="broken-shape">
    <div class="line"></div>
    <div class="shape">
      <div class="inner-wrapper">
        <div class="lifestyle"><p>Lifestyle</p></div>
      </div>
    </div>
  </div>
</template>

<script>
</script>

<style>
.broken-shape {
  width: 360px;
  height: 250px;
  position: relative;
}

.line {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  margin: 0 auto;
  z-index: 2;
  width: 25px;
  height: 100%;
  background-color: #ffffff;
}

.broken-shape .broke-shape {
  top: 0;
  position: absolute;
  z-index: 1;
}

.shape {
  width: 360px;
  height: 250px;
  box-shadow: 0 0 0 rgba(0, 0, 0, 0.1);
  border: 6px solid #ffffff;
  background: rgba(128, 128, 128, 1);
  display: flex;
  justify-content: center;
}

.inner-wrapper {
  width: 147px;
  height: 49px;
  border: 1px solid #ffffff;
  display: flex;
  justify-content: center;
  align-self: center;
}

.lifestyle {
  z-index: 3;
  width: 133px;
  height: 36px;
  background-color: #ffffff;
  display: flex;
  justify-content: center;
  align-self: center;
}

.lifestyle p {
  align-self: center;
  font-family: var(--page-font);
  align-self: center;
  font-size: 12px;
  font-weight: 700;
  text-transform: uppercase;
  color: #3e3e3e;
}

</style>