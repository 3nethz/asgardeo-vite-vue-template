<script setup>
import { useAsgardeo } from '@asgardeo/vue'
import { computed } from 'vue'

const { state, signOut } = useAsgardeo()

const userEmail = computed(() => state?.email || 'This is the content of the home page.')
</script>

<template>
  <div>
    <h1>Welcome to the Home Page!</h1>
    <p>{{ userEmail }}</p>
    <button @click="signOut">Sign Out</button>
  </div>
</template>
