<script setup lang="ts">
import { ref } from "vue";

defineProps<{ msg: string[] }>();

const count = ref(0);
const es = ref(true);
</script>

<template>
  <h1>{{ es ? msg[1] : msg[0] }}</h1>

  <div class="card">
    <button type="button" @click="count++">
      {{ (!es ? "count is " : "El contador es ") + count }}
    </button>
    <button type="button" @click="es = !es">
      {{ es ? "Cambia el idioma" : "Change the language" }}
    </button>
  </div>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
