<template>
  <text class="space" height="0px" :id="label + '.space'">-</text>
  <span class="NAword">
    <span
      class="NAspan"
      v-for="n in splitLabel.length"
      :id="label + '.' + (n - 1)"
      :key="splitLabel[n - 1]"
      height="min-content"
    >
      {{ splitLabel[n - 1] }}
    </span>
  </span>
</template>

<style>
.NAspan {
  opacity: 0;
  display: inline-block;
  height: 2px;
}
.NAword {
  display: inline-block;
}
.space {
  width: 0;
  height: 2px;
  opacity: 0;
  transition: 0.6s;
  display: inline-block;
}
.minus {
  width: 0px;
  opacity: 0;
  transform: translateX(-3vmax);
  transition: width v-bind(letterTimeS), transform 0.4s, opacity 0.1s ease-in;
}
.fade {
  opacity: 1;
  transform: translateX(0);
  transition: width v-bind(letterTimeE), transform 0.3s ease,
    opacity 0.5s ease-out;
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
      splitLabel: this.label.split(""),
      wait: Date.now(),
      letterTimeE: 1500 / this.label.length + "ms",
      letterTimeS: 2500 / this.label.length + "ms",
    };
  },
  watch: {
    //Watch function to activate on extend variable change
    extend(val) {
      if (val) {
        //Timeout to have the shortening and extending not overlap
        setTimeout(() => {
          if (this.wait - Date.now() <= 0) {
            this.animateExtension();
          }
        }, this.wait - Date.now());
      } else {
        //Timeout to have the shortening and extending not overlap
        this.wait = Date.now() + 500;
        setTimeout(() => {
          if (!this.extend) {
            this.animateShortening();
            this.wait = Date.now() + 500;
          }
        }, this.wait - Date.now());
      }
    },
  },
  methods: {
    //
    // ---Animate extension sub-functions---
    //
    classPerLetterE(n, time) {
      let label = this.label;
      const span = document.getElementById(label + "." + n);
      span.classList.add("fade");
      span.style.width = span.scrollWidth + "px";
      //Expanding the width of the span elements one by one manually
      if (n > 1) {
        setTimeout(() => {
          this.classPerLetterE(n - 1, time);
        }, time);
      } else {
        //Animating the space behind the word
        const span = document.getElementById(label + ".space");
        span.style.transition = this.letterTimeE;
        span.style.width = span.scrollWidth + "px";
      }
    },
    //Function to add the class and function that animate the extension of the characters
    animateExtension() {
      let label = this.label;

      this.classPerLetterE(label.length - 1, 100 / label.length);
    },
    //
    // ---Animate Shortening sub-functions---
    //
    classPerLetterS(n, time) {
      let label = this.label;
      const span = document.getElementById(label + "." + n);
      span.classList.remove("fade");
      span.style.width = "0px";
      //Expanding the width of the span elements one by one manually
      if (n > 1) {
        setTimeout(() => {
          this.classPerLetterS(n - 1, time);
        }, time);
      } else {
        //Animating the space behind the word
        const span = document.getElementById(label + ".space");
        span.style.transition = this.letterTimeS;
        span.style.width = "0px";
      }
    },
    //Function to add the class and function that animate the shortening of the characters
    animateShortening() {
      this.classPerLetterS(this.label.length - 1, 300 / this.label.length);
    },
  },
  mounted() {
    //Initial asignation of classes
    let span = document.getElementById(this.label + "." + 0);
    span.style.opacity = "1";
    for (let n = 1; n < this.label.length; n++) {
      let span = document.getElementById(this.label + "." + n);
      span.classList.add("minus");
    }
  },
  setup() {
    return {};
  },
};
</script>
