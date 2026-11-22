<template>
  <section>
    <!--Components -->
    <AppHeader />
    <h1>Homepage</h1>
    <!--Component names-->
    <BaseButton />
    <BaseCard />
    <!--Dynamic components-->
    <component :is="dynamicComponent"></component>
    <component :is="SecondaryButton"></component>
    <br />
    <br />
    <component :is="dynamicView"></component>
    <button @click="toggleView">Toggle View</button>
  </section>
</template>
<script setup>
import { SecondaryButton, GridView, ListView } from "#components";
const dynamicComponent = resolveComponent("PrimaryButton");

const view = ref("grid");
const components = {
  grid: GridView,
  list: ListView,
};

const dynamicView = computed(() => components[view.value]);
const toggleView = () => {
  view.value = view.value === "grid" ? "list" : "grid";
};
</script>
