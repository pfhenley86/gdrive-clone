<script setup>

// Imports
import { Link } from '@inertiajs/vue3'
import ApplicationLogo from "@/Components/ApplicationLogo.vue";
import CreateNewDropdown from "@/Components/app/CreateNewDropdown.vue";
import NavLink from "@/Components/NavLink.vue";
// Uses

// Refs

// Props & Emit

// Computed

// Methods

// Hooks

</script>

<style scoped>

</style>

<template>
    <nav class="min-w-[200px]">
        <div class="h-[80px] px-3 flex items-center gap-3">
            <Link href="/">
                <ApplicationLogo class="block w-auto text-gray-800 fill-current h-9" />
            </Link>
            LaraStorage
        </div>
        <div class="px-3">
            <CreateNewDropdown />

            <div class="py-3">
                <NavLink href="/">My Files</NavLink>
                <NavLink href="/" :active="true">Shared with Me</NavLink>
                <NavLink href="/">Shared by Me</NavLink>
                <NavLink href="/" :active="true">Trash</NavLink>
            </div>
        </div>
    </nav>
</template>
