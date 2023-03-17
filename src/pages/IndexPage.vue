<template>
  <q-page
    class="flex flex-top CenturyGothic bg-primary"
    style="overflow-x: hidden"
  >
    <body style="position: relative; left: 10px">
      <!--This section is used to animate my name-->
      <h1 class="text-accent">Jason Piedra Matamoros</h1>
      <h1 class="text-accent">JasonPM</h1>
      <q-btn color="secondary" text-color="primary"><b>Change</b></q-btn>
      <!---->
    </body>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "IndexPage",
});
</script>
