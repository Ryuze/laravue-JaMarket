<template>
    <Head title="Dashboard Product" />

    <dashboard>
        <div class="container mx-auto">
            <div class="flex flex-col">
                <div class="flex flex-row-reverse">
                    <button-tailwind :type="'button'" :class="'bg-green-500 hover:bg-green-600'">
                        Add product
                    </button-tailwind>
                </div>
            </div>
        </div>
    </dashboard>
</template>

<script>
import { Head } from '@inertiajs/inertia-vue3';
import Dashboard from '@/Layouts/Dashboard.vue';
import ButtonTailwind from "@/Components/ButtonTailwind.vue";

export default {
    setup() {
        return {};
    },
    components: {
        Head,
        Dashboard,
        ButtonTailwind
    }
};
</script>

<style scoped></style>
