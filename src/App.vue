<template>
  <v-app>
    <v-main>
      <InlineEditor />
    </v-main>
  </v-app>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import InlineEditor from "./components/InlineEditor.vue";

export default defineComponent({
  name: "App",

  components: {
    InlineEditor,
  },

  data() {
    return {
      //
    };
  },
});
</script>
