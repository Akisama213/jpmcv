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
template {
  width: fit-content;
}
span {
  opacity: 0;
}
.minus {
  opacity: 0;
  transition: all 0.3s ease-out;
  transform: translateX(-50px);
  display: inline-block;
  width: 0%;
}
.mayus {
  width: initial;
  opacity: 1;
}
.space {
}
.space::before {
  content: " ";
}
.fade {
  transition: all 0.3s ease-out;
  width: initial;
  opacity: 1;
  transform: translateX(0);
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
      wait: Date.now(),
    };
  },
  watch: {
    extend(val) {
      console.log("Pre extend", val);
      if (val) {
        setTimeout(this.animateExtension, this.wait - Date.now());
      } else {
        this.wait = Date.now() + 200;
        setTimeout(() => {
          if (!this.extend) {
            console.log(this.extend);
            this.animateShortening();
          } else {
            this.wait = Date.now() + 500;
          }
        }, this.wait - Date.now());
      }
    },
  },
  methods: {
    animateExtension() {
      let timer = setInterval(onTick, 180 / this.label.length);
      let n = this.label.length - 1;
      let label = this.label;
      const space = document.getElementById(label + "." + 0);
      space.classList.add("space");
      function onTick() {
        if (n > 0) {
          const span = document.getElementById(label + "." + n);
          span.classList.add("fade");
          n--;
          //console.log(span);
        } else {
          clearInterval(timer);
          timer = null;
        }
      }
    },
    animateShortening() {
      let timer = setInterval(onTick, 300 / this.label.length);
      let n = 0;
      let label = this.label;
      const space = document.getElementById(label + "." + 0);
      space.classList.remove("space");
      function onTick() {
        if (n < label.length) {
          const span = document.getElementById(label + "." + n);
          span.classList.remove("fade");
          n++;
        } else {
          clearInterval(timer);
          timer = null;
        }
      }
      this.wait = Date.now() + 600;
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
