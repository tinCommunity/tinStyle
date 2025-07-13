<template>
  <input class="input" v-bind="$attrs" />
</template>

<script setup lang="ts">
defineOptions({
  inheritAttrs: true
});
</script>

<style scoped>
.input {
  padding: 8px 12px;
  border: 1px solid #ccc;
  border-radius: 4px;
}
</style>