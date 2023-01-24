<template>
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
</template>
<script setup lang="ts">
useHead({
  titleTemplate:(titleChunk)=>{
    return titleChunk ? `${titleChunk} - My movie site` : 'My movie site'
  }
})
</script>
