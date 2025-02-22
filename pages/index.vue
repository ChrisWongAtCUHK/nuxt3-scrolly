<template>
  <ol>
    <li v-for="index in 100" :key="index">
      <NuxtLink :href="`/session/${index}`" @click.prevent="setScrollY()">Thing {{ index }}</NuxtLink>
    </li>
  </ol>
  <LazyNuxtPage />
</template>
<script lang="ts" setup>
  const setScrollY = (e) => {
    const scrollY = useState('counter', () => window.scrollY)
  }
</script>