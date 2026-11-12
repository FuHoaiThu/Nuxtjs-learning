<template>
  <div>
    <NuxtPage />
  </div>
</template>
<script setup>
useHead({
  title: "Awesome App",
  meta: [
    {
      name: "description",
      content: "Some description...",
    },
  ],
  link: [
    {
      rel: "stylesheet",
      href: 'https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/css/bootstrap.min.css'
    }
  ]
});
</script>
