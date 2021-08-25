<template>
    <Head title="Dashboard" />

    <dashboard />
</template>

<script>
import { Head } from '@inertiajs/inertia-vue3';
import Dashboard from '@/Layouts/Dashboard.vue';

export default {
    components: {
        Head,
        Dashboard,
    },
}
</script>
