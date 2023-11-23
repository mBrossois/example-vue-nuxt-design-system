<script setup lang="ts">
import { ref } from 'vue'

defineProps<{ text: string }>()

const emit = defineEmits<{
    (e: 'clicked', value: number): void;
  }>();

const count = ref(0)

function onClick() {
  count.value++;
  emit('clicked', count.value)
}
</script>

<template>
  <button @click="onClick()">{{ text }}</button>
</template>

<style scoped>

</style>
