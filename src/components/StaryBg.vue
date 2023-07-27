<template class=".SBtemplate">
  <div id="SBbg" class="SBdiv"></div>
</template>
<style>
.SBtemplate {
  background-image: linear-gradient(to right, black, transparent);
}
.SBdiv {
  background: radial-gradient(rgba(0, 0, 0, 1) 8%, transparent 20%);
  background-position: 0% 0%;
  background-size: 5vmin 5vmin;
  position: absolute;
  top: -90%;
  left: -120%;
  rotate: -15deg;
  height: 100%;
  width: 100%;
  z-index: -100;
  opacity: 15%;
  transition: all 1s ease-out;
  animation: SBmove 30s linear infinite;
}
.SBhold {
  left: -115%;
  opacity: 30%;
  transition: all 1s ease;
  height: 130%;
  width: 130%;
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
  props: {
    extend: { default: false, type: Boolean },
  },
  watch: {
    extend(val) {
      if (val) {
        this.add();
      } else {
        this.remove();
      }
    },
  },
  methods: {
    add() {
      const bg = document.getElementById("SBbg");
      console.log(bg);
      bg.classList.add("SBhold");
    },
    remove() {
      const bg = document.getElementById("SBbg");
      bg.classList.remove("SBhold");
    },
  },
  setup() {
    return {};
  },
};
</script>
