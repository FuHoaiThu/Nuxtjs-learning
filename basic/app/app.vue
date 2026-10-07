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
      content: "Some description ....",
    },
  ],
  link: [
    {
      rel: "stylesheet",
      href: "https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.8/js/bootstrap.min.js",
    },
  ],
});
</script>
