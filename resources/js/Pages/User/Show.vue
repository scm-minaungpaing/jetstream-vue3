<script setup>
import AppLayout from '@/Layouts/AppLayout.vue';
import { Link } from '@inertiajs/inertia-vue3'

const props = defineProps({
  user: Object,
});
</script>

<template>
    <AppLayout title="Dashboard">
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">
                User
            </h2>
        </template>

        <div class="py-12">
            <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
                <div class="-mx-4 sm:-mx-8 px-4 sm:px-8 py-4 overflow-x-auto">
                    {{ 'name:' + user.name}} <br/>
                    {{'email:' + user.email}} <br/>
                    {{'created_at: ' + user.created_at}} <br/>
                    {{'updated_at: ' + user.updated_at}} <br/>
                </div>
            </div>
        </div>
    </AppLayout>
</template>
