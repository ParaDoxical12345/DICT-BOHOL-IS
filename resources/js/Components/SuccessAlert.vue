<script setup>
import { ref } from 'vue';

const isVisible = ref(true);

const emits = defineEmits(['close']);
</script>

<template>
    <div v-if="isVisible" class="flex p-4 space-x-3 rounded-lg bg-green-200">
        <div class="shrink-0">
            <span>
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-6 h-6 text-green-700">
                <path fill-rule="evenodd" d="M2.25 12c0-5.385 4.365-9.75 9.75-9.75s9.75 4.365 9.75 9.75-4.365 9.75-9.75 9.75S2.25 17.385 2.25 12Zm13.36-1.814a.75.75 0 1 0-1.22-.872l-3.236 4.53L9.53 12.22a.75.75 0 0 0-1.06 1.06l2.25 2.25a.75.75 0 0 0 1.14-.094l3.75-5.25Z" clip-rule="evenodd" />
                </svg>
            </span>
        </div>
        <div class="flex-1">
            <h1 class="text-lg font-semibold text-green-700">Success!</h1>
            <p class="text-green-700">
                <slot />
            </p>
        </div>
        <div class="shrink-0">
            <button type="button" @click="emits('close')" class="hover:bg-green-300 rounded-lg hover:text-green-700 p-1">
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5">
                <path stroke-linecap="round" stroke-linejoin="round" d="M6 18 18 6M6 6l12 12" />
                </svg>
            </button>
        </div>
    </div>
</template>