<template class=".SBtemplate">
  <div class="SBdiv"></div>
</template>
<style>
.SBtemplate {
  background-image: linear-gradient(to right, black, transparent);
}
.SBdiv {
  background: radial-gradient(rgba(255, 255, 255, 0.1) 5%, transparent 10%);
  background-position: 0% 0%;
  background-size: 5vmin 5vmin;
  position: absolute;
  top: -90%;
  left: -90%;
  rotate: -15deg;
  height: 100%;
  width: 100%;
  z-index: -100;
  animation: SBmove 10s linear infinite;
}
@keyframes SBmove {
  from {
    background-position: 0% 0%;
  }
  to {
    background-position: -100% 0%;
  }
}
</style>
<script>
export default {
  name: "StaryBg",

  setup() {
    return {};
  },
};
</script>
