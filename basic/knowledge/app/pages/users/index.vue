<template>
  <h1>Users</h1>
</template>
<script setup>
definePageMeta({
  title: "User Page",
  meta: [
    {
      name: "description",
      content: "User page description...",
    },
  ],
});

const route = useRoute()
console.log(route.meta)
useHead(route.meta)
</script>
