<template>
    <button :class="finalClass" v-bind="$attrs">
        <slot />
    </button>
</template>

<script setup>
import { computed } from 'vue';

const props = defineProps({ class: String });
const finalClass = computed(() =>
    `px-4 py-2 rounded bg-blue-600 text-white hover:bg-blue-700 transition ${props.class || ''}`
);
</script>