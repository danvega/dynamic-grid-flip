<template>
  <vue-flip :active-hover="true" width="100%" height="100%" class="simple-test">
    <div slot="front">
      <img :src="require('@/assets/img/codesandbox-custom-theme-cover.png')" />
    </div>
    <div slot="back">back</div>
  </vue-flip>
</template>

<script>
import VueFlip from "vue-flip";

export default {
  components: {
    "vue-flip": VueFlip
  }
};
</script>

<style>
.simple-test {
  width: 1000px;
  height: 492px;
  cursor: pointer;
}
.back {
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #673ab7;
  color: white;
}
</style>
