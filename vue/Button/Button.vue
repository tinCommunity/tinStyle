<template>
  <button class="btn" @click="$emit('click', $event)">
    <slot />
  </button>
</template>

<script setup lang="ts">
const emit = defineEmits<{
  (e: 'click', event: MouseEvent): void
}>();
</script>

<style scoped>
.btn {
  padding: 8px 16px;
  background-color: #4f46e5;
  color: white;
  border: none;
  border-radius: 6px;
  cursor: pointer;
}
</style>