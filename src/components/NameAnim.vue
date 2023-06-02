<template>
  <text class="space" :id="label + '.space'">-</text>
  <span class="visible">
    <span
      v-for="n in SplitLabel.length"
      :id="label + '.' + (n - 1)"
      :key="SplitLabel[n - 1]"
    >
      {{ SplitLabel[n - 1] }}
    </span>
  </span>
</template>

<style>
span {
  opacity: 0;
  display: inline-block;
}
.space {
  width: 0;
  opacity: 0;
  transform: translateX(50px);
  transition: 0.6s;
  display: inline-block;
}
.visible {
  opacity: 1;
}
.spaced {
  width: auto;
  transform: translateX(0px);
  transition: width 0.3s;
}
.minus {
  width: 0;
  opacity: 0;
  transform: translateX(-50px);
  transition: transform 0.4s ease, opacity 0.1s ease-out;
}
.fade {
  opacity: 1;
  transform: translateX(0);
  transition: transform 0.3s ease, opacity 0.2s ease-out;
}
</style>

<script>
// transition: transform 0.4s ease, opacity 0.15s;
// transition: transform 0.3s ease, opacity 0.1s;
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
      extended: false,
    };
  },
  watch: {
    //Watch function to activate on extend variable change
    extend(val) {
      if (val) {
        //Timeout to have the shortening and extending not overlap
        setTimeout(() => {
          if (!this.extended) {
            this.animateExtension();
            this.extended = true;
          }
        }, this.wait - Date.now());
      } else {
        //Timeout to have the shortening and extending not overlap
        this.wait = Date.now() + 300;
        setTimeout(() => {
          if (!this.extend & this.extended) {
            this.animateShortening();
            this.extended = false;
          }
        }, this.wait - Date.now());
      }
    },
  },
  methods: {
    //Function to add the class and function that animate the extension of the characters
    animateExtension() {
      let label = this.label;
      let length = label.length;
      let timer = setInterval(onTick, 180 / length);
      let n = length - 1;

      //Animating the space behind the word
      const span = document.getElementById(label + ".space");
      span.classList.add("spaced");
      let show_timer = setInterval(show_onTick, 20 / length);
      let show_n = 0;
      function show_onTick() {
        show_n += 2;
        if (show_n < span.scrollWidth) {
          span.style.width = show_n + "px";
        } else {
          clearInterval(show_timer);
          show_timer = null;
        }
      }

      function onTick() {
        if (n > 0) {
          const span = document.getElementById(label + "." + n);
          span.classList.add("fade");
          n--;

          //Expanding the width of the span elements one by one manually
          let show_timer = setInterval(show_onTick, 20 / length);
          let show_n = 0;
          function show_onTick() {
            show_n += 2;
            if (show_n < span.scrollWidth) {
              span.style.width = show_n + 1 + "px";
            } else {
              clearInterval(show_timer);
              show_timer = null;
            }
          }
        } else {
          clearInterval(timer);
          timer = null;
        }
      }
    },
    //Function to add the class and function that animate the shortening of the characters
    animateShortening() {
      let label = this.label;
      let length = label.length;
      let timer = setInterval(onTick, 300 / length);
      let n = length - 1;

      //Animating the space behind the word
      const span = document.getElementById(label + ".space");
      span.classList.remove("spaced");
      let hide_n = span.scrollWidth;
      let hide_timer = setInterval(hide_onTick, 20 / length);
      function hide_onTick() {
        hide_n -= 2;
        if (hide_n > 0) {
          span.style.width = hide_n - 1 + "px";
        } else {
          clearInterval(hide_timer);
          hide_timer = null;
        }
      }

      this.wait = Date.now() + 300;
      function onTick() {
        if (n > 0) {
          const span = document.getElementById(label + "." + n);
          span.classList.remove("fade");
          n--;

          //Shortening the width of the span elements one by one manually
          let hide_n = span.scrollWidth;
          let hide_timer = setInterval(hide_onTick, 20 / length);
          function hide_onTick() {
            hide_n -= 2;
            if (hide_n > 0) {
              span.style.width = hide_n - 1 + "px";
            } else {
              clearInterval(hide_timer);
              hide_timer = null;
            }
          }
        } else {
          clearInterval(timer);
          timer = null;
        }
      }
      this.wait = Date.now() + 300;
    },
  },
  mounted() {
    //Initial asignation of classes
    const span = document.getElementById(this.label + "." + 0);
    span.classList.add("visible");
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
