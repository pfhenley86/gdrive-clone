<script setup>
import Navigation from '@/Components/app/Navigation.vue';
import SearchForm from '@/Components/app/SearchForm.vue';
import UserSettingsDropdown from '@/Components/app/UserSettingsDropdown.vue';
</script>

<template>
    <div class="flex w-full h-screen gap-4 bg-gray-50">
        <Navigation />

        <main class="flex flex-col flex-1 px-4 overflow-hidden">
            <div class="flex items-center justify-between w-full">
                <SearchForm />
                <UserSettingsDropdown />
            </div>
            <div class="flex flex-col flex-1 overflow-hidden">
                <slot />
            </div>
        </main>
    </div>
</template>
