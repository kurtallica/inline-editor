<template>
  <v-container>
    <div id="main" align="center" justify="center" v-cloak @click="hideTooltip">
      <div class="tooltip" @click.stop v-if="show_tooltip">
        <v-text-field
          label="Filled"
          filled
          v-model="text_content"
        ></v-text-field>
      </div>
      <p @click.stop="toggleTooltip">✎ {{ text_content }}</p>
    </div>
  </v-container>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "InlineEditor",

  data() {
    return {
      show_tooltip: false,
      text_content: "Edit Me.",
    };
  },
  methods: {
    hideTooltip: function () {
      this.show_tooltip = false;
    },
    toggleTooltip: function () {
      this.show_tooltip = !this.show_tooltip;
    },
  },
});
</script>

<style scoped>
[v-cloak] {
  display: none;
}
* {
  margin: 0;
  padding: 0;
}
</style>
