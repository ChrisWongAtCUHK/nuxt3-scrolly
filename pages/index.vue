<template>
  <ol>
    <li v-for="index in 100" :key="index">
      <NuxtLink :href="`/session/${index}`">Thing {{ index }}</NuxtLink>
    </li>
  </ol>
  <LazyNuxtPage />
</template>
