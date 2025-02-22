<script setup lang="ts">
import { useRoute, useRouter } from "vue-router";
import { watch } from "vue";

const route = useRoute();
const router = useRouter();

onMounted(() => {
  setTimeout(()=> {
    const scrollY = useState("counter");
    window.scroll(0, scrollY.value);
  }, 10)
});
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
