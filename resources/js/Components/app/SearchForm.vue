<script setup>

// Imports
import { useForm } from '@inertiajs/vue3';
import TextInput from "@/Components/TextInput.vue";

// Uses
const form = useForm({
    search: '',
});

// Refs

// Props & Emit

// Computed

// Methods

// Hooks

</script>

<style scoped>

</style>

<template>
    <form class="w-[600px] h-[80px] flex items-center">
        <TextInput type="text" class="block w-full mr-2" v-model="form.search" autocomplete placeholder="Search for files and folders" />
    </form>
</template>
