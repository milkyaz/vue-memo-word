<script setup>
import BaseButton from "./components/BaseButton.vue";
</script>

<template>
  <main class="main">
    <BaseButton>Начать игру</BaseButton>
  </main>
</template>
<style scoped>
.main {
  display: grid;
  place-items: center;
  min-height: 100vh;
}
</style>
