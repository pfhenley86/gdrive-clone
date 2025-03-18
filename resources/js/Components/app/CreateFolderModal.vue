<script setup>

// Imports
import { Modal } from '@headlessui/vue';
import InputLabel from 'vendor/laravel/breeze/stubs/inertia-react/resources/js/Components/InputLabel';
import TextInput from 'vendor/laravel/breeze/stubs/inertia-react/resources/js/Components/TextInput';

// Uses

// Refs

// Props & Emit
const { modelValue } = defineProps({
  modelValue: Boolean
})

// Computed

// Methods

// Hooks

</script>

<style scoped>

</style>

<template>
    <Modal :show="modelValue">
        <div class="p-6">
            <h2 class="text-lg font-medium text-gray-900">
                Create New Folder
            </h2>
            <div class="mt-6">
                <InputLabel for="folderName" value="folderName" />
                <TextInput type="text"
                           id="folderName" v-model="form.name"
                           class="block w-full mt-1"
                           :class="form.errors.name ? 'border-red-500 focus:border-x-red-500 focus:ring-red-500' : ''"
                           placeholder="Folder Name"
                           @keyup.enter="createFolder" />
                />
                <InputError :message="form.errors.name" />
            </div>
        </div>
    </Modal>
</template>
