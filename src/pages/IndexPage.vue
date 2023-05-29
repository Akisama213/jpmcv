<template>
  <q-page class="CenturyGothic" style="overflow-x: hidden">
    <!--This section is used to animate my name-->
    <div @mouseover="extend = true" @mouseleave="extend = false">
      <h1 class="text-accent">
        Jason<NameAnim label="Piedra" :extend="extend" />
        <NameAnim label="Matamoros" :extend="extend" />
      </h1>
    </div>
    <!---->
    <div>
      <text v-for="n in 300" :key="n">Hello, this is "nothing" text. </text>
    </div>
  </q-page>
</template>

<script>
import NameAnim from "../components/NameAnim.vue";
export default {
  name: "IndexPage",
  data() {
    return {
      extend: false,
    };
  },
  methods: {
    getExtend() {
      return this.extend;
    },
  },
  watch: {},
  mounted() {
    /*setInterval(OnTick, 10);

    function OnTick() {
      extend = this.getExtend();
      console.log("Is extend true?", this.extend);
    };*/
  },
  components: {
    NameAnim,
  },
};
</script>
