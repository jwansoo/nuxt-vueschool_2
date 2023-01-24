<template>
  <div>
    <nav style="display:flex; gap:10px">
      <NuxtLink to="/">Home</NuxtLink>
      <NuxtLink to="/movies">Movies</NuxtLink>
      <NuxtLink to="https://vueschool.io">Vue School</NuxtLink>
      <NuxtLink v-if="!user.isLoggedIn" to="/login">Login</NuxtLink>
      <a href="#" v-else @click.prevent="user.isLoggedIn=false">Logout</a>
      test
    </nav>
    <slot></slot>
  </div>
</template>
<script setup lang="ts">
import { useUser } from '~~/stores/User';

const user=useUser()
</script>