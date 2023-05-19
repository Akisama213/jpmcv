<template class="CenturyGothic">
  <router-view />
</template>

<script>
import { defineComponent } from "vue";
import { useQuasar } from "quasar";

export default defineComponent({
  name: "App",

  setup() {
    const $q = useQuasar();
    $q.addressbarColor.set("#a2e3fa");
  },
});
</script>
