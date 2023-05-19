<template>
  <q-page
    class="flex flex-top CenturyGothic bg-primary"
    style="overflow-x: hidden"
  >
    <body style="position: relative; left: 10px">
      <!--This section is used to animate my name-->
      <div @mouseover="extend()" @mouseleave="shorten()">
        <div :hidden="extended">
          <h1 class="text-accent">Jason Piedra Matamoros</h1>
        </div>
        <div :hidden="shortened">
          <h1 class="text-accent">JasonPM</h1>
        </div>
        <!--q-btn
        color="secondary"
        text-color="primary"
        @click="name_toggle()"
        :loading="loading"
      >
        <b>Change</b>
      </q-btn--->
      </div>
      <!---->
    </body>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "IndexPage",
  data() {
    return {
      extended: true,
      shortened: false,
    };
  },

  methods: {
    /* Learnt a lot from this
    name_toggle() {
      //Changing between extended and shortened versions of my name
      if (this.hover) {
        this.shortened = true;
        this.extended = false;
      } else {
        this.shortened = false;
        this.extended = true;
      }*/
    extend() {
      if (this.extended) {
        this.shortened = true;
        this.extended = false;
      }
    },
    shorten() {
      if (this.shortened) {
        this.shortened = false;
        this.extended = true;
      }
      /*
      this.shortened = false;
      this.extended = true;
    */
    },
  },
});
</script>
