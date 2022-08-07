<script setup lang="ts">
const touches = [1, 2, 3, 4, 5, 6, 8]
</script>

<template>
  <PianoTouche v-for="(touche, idx) in touches" :key="idx" :note="touche" />
</template>

