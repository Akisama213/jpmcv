<template>
  <span label=" " :id="label + '.' + 'space'" />
  <span
    v-for="n in SplitLabel.length"
    :id="label + '.' + (n - 1)"
    :key="SplitLabel[n - 1]"
  >
    {{ SplitLabel[n - 1] }}
  </span>
</template>

<style>
span.minus {
  opacity: 0;
  transition: all 0.3s ease-in-out;
  transform: translateX(-width);
  display: inline-block;
  width: 0%;
}
span.mayus {
  width: auto;
  opacity: 1;
  transform: translateX(width);
}
span.minus.fade {
  transition: all 0.5s ease-in-out;
  width: auto;
  opacity: 1;
  transform: translateX(width);
}
</style>

<script>
export default {
  name: "NameAnim",
  props: {
    label: { required: true, type: String },
    extend: { default: false, type: Boolean },
  },
  data() {
    return {
      SplitLabel: this.label.split(""),
    };
  },
  watch: {
    extend(val) {
      let timer = null;
      if (val) {
        while (timer === null) {
          //console.log("Extending");
          timer = this.animateExtension();
          console.log("timer", timer);
        }
      } else {
        while (timer === null) {
          //console.log("Shortening");
          timer = this.animateShortening();
        }
      }
    },
  },
  methods: {
    animateExtension() {
      let timer = setInterval(onTick, 30);
      let n = this.label.length - 1;
      let label = this.label;
      const space = document.getElementById(label + "." + "space");
      space.classList.add("fade");
      function onTick() {
        if (n > 0) {
          const span = document.getElementById(label + "." + n);
          span.classList.add("fade");
          //console.log(span);
          n--;
        } else {
          clearInterval(timer);
          timer = null;
        }
      }
      return timer;
    },
    animateShortening() {
      let timer = setInterval(onTick, 30);
      let n = 0;
      let label = this.label;
      const space = document.getElementById(label + "." + "space");
      space.classList.remove("fade");
      function onTick() {
        if (n < label.length) {
          const span = document.getElementById(label + "." + n);
          span.classList.remove("fade");
          //console.log(span);
          n++;
        } else {
          clearInterval(timer);
          timer = null;
        }
      }
      return timer;
    },
  },
  mounted() {
    const span = document.getElementById(this.label + "." + 0);
    span.classList.add("mayus");
  },
  setup() {
    return {};
  },
};
</script>
