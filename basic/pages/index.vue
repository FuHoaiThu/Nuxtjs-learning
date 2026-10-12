<template>
  <main>
    <h1>Homepage</h1>
    <hr />
    <Card />
    <hr />
    <UsersProfile />
    <hr />
    <Detail />
    <hr />
    <UsersInformation />
  </main>
</template>
<script setup>
import Detail from "~/components/users/detail.vue";
import { UsersInformation } from "#components";
</script>
