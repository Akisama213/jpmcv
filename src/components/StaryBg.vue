<template class=".SBtemplate">
  <div id="SBbg" class="SBdiv"></div>
</template>
<style>
.SBtemplate {
  background-image: linear-gradient(to right, black, transparent);
}
.SBdiv {
  background: radial-gradient(black 50%, transparent 35%);
  background-position: 0% 0%;
  background-size: 4vmin 4vmin;
  position: absolute;
  top: -55vmin;
  left: -50vmin;
  rotate: -14deg;
  height: 80vmin;
  width: 80vmin;
  z-index: -100;
  opacity: 15%;
  transition: all 1s ease;
  animation: SBmove 30s linear infinite;
  mask-image: radial-gradient(black, transparent 90%);
  mask-mode: alpha;
}
.SBhold {
  top: -85vmin;
  left: -40vmin;
  opacity: 30%;
  transition: all 1s;
  height: 120vmin;
  width: 120vmin;
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
