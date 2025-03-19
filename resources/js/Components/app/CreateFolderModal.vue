<script setup>

// Imports
import { Modal } from '@headlessui/vue';
import InputLabel from '@Components/InputLabel';
import { useForm } from '@inertiajs/vue3';
import InputError from '@Components/InputError';
import TextInput from '@Components/TextInput';
import SecondaryButton from '@Components/SecondaryButton.vue';

// Uses
const form = useForm({
    name: ''
})

// Refs

// Props & Emit
const { modelValue } = defineProps({
  modelValue: Boolean
})

const emit = defineEmits(['update:modelValue']);

// Computed

// Methods
function createFolder(){
    console.log('Create Folder');
}

function closeModal(){
    emit('update:modelValue');
}

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
                <InputError :message="form.errors.name" class="mt-2" />
            </div>
            <div class="flex justify-end mt-6">
                <SecondaryButton @click="closeModal">Cancel</SecondaryButton>
            </div>
        </div>
    </Modal>
</template>
