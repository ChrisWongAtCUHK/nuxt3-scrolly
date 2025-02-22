<script setup lang="ts">
import { useRoute, useRouter } from "vue-router";
import { watch } from "vue";

const route = useRoute();
const router = useRouter();
</script>

<template>
  <div
    :style="{
      position: 'fixed',
      top: '16px',
      right: '16px',
      backgroundColor: '#cccccc',
      padding: '8px',
    }"
  >
    Thing {{ route.params.id }}.
    <button @click="router.push('/')">(Close overlay)</button>
  </div>
</template>
