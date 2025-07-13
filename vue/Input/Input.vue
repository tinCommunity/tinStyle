<template>
    <input :class="finalClass" v-bind="$attrs" />
</template>

<script setup>
import { computed } from 'vue';

const props = defineProps({ class: String });
const finalClass = computed(() =>
    `px-3 py-2 border border-gray-300 rounded outline-none focus:ring-2 focus:ring-blue-500 ${props.class || ''}`
);
</script>