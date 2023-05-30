<template>
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
  transform: translateX(-5%);
  display: inline-block;
  width: 0%;
}
span.mayus {
  transition: all 1s ease-in-out;
  width: auto;
  opacity: 1;
}
span.mayus.space {
  transition: all 1s ease-in-out;
}
span.mayus.space::before {
  content: " ";
}
span.minus.fade {
  transition: all 0.6s ease-in-out;
  width: fit-content;
  opacity: 1;
  transform: translateX(5%);
}
</style>

<script>
import { thisExpression } from "@babel/types";

export default {
  name: "NameAnim",
  props: {
    label: { required: true, type: String },
    extend: { default: false, type: Boolean },
  },
  data() {
    return {
      SplitLabel: this.label.split(""),
      active: true,
    };
  },
  watch: {
    extend(val) {
      if (val) {
        console.log("In timer", this.timer);
        while (this.timer != null) {
          //console.log("Extending");
          this.timer = this.animateExtension();
          console.log("timer", this.timer);
        }
        console.log("Out timer", this.timer);
        this.timer = true;
      } else {
        console.log("In timer", this.timer);
        while (this.timer != null) {
          //console.log("Extending");
          this.timer = this.animateShortening();
          console.log("timer", this.timer);
        }
        console.log("Out timer", this.timer);
        this.timer = true;
      }
    },
  },
  methods: {
    animateExtension() {
      let timer = setInterval(onTick, 30);
      let n = this.label.length - 1;
      let label = this.label;
      const space = document.getElementById(label + "." + 0);
      space.classList.add("space");
      console.log(space);
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
      return null;
    },
    animateShortening() {
      let timer = setInterval(onTick, 30);
      let n = 0;
      let label = this.label;
      const space = document.getElementById(label + "." + 0);
      space.classList.remove("space");
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
      return null;
    },
  },
  mounted() {
    const span = document.getElementById(this.label + "." + 0);
    span.classList.add("mayus");
    for (let n = 1; n < this.label.length; n++) {
      const span = document.getElementById(this.label + "." + n);
      span.classList.add("minus");
    }
  },
  setup() {
    return {};
  },
};
</script>
