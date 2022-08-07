<script setup lang="ts">
const props = defineProps<{
  note: number
}>()

const AhPiano = () => {
  const audio = new Audio(`/sound/${props.note}.mp3`)
  audio.play()
}
</script>

<template>
  <div v-if="note % 2 === 0" class="h-[calc(100vh/4)] w-[calc(100vw)] bg-white border-black border-1" @click="AhPiano()" />
  <div v-else class="w-[calc(50vw)] h-[calc(100vh/6)] border-black bg-black border-2 absolute right-0 mt-[calc(100vh/6)]" @click="AhPiano()" />
</template>
