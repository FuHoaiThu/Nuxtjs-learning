<template>
  <h1>Homepage</h1>
  <nuxt-link to="https://www.google.com/" target="_blank"
    >Go to google</nuxt-link
  >
  <hr />
  <button @click="router.push('/contact')">Go to contact</button>
</template>
<script setup>
const router = useRouter();
</script>
