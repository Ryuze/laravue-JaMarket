<template>
    <div class="relative max-h-screen">
        <div class="flex flex-col">
            <div class="fixed w-screen">
                <dashboard-header />
            </div>
            <div class="absolute mt-16">
                <div class="fixed overflow-auto hidden md:block">
                    <dashboard-sidepanel />
                </div>
                <div class="md:ml-68 md:mt-2 ml-2 mt-2 overflow-auto">
                    <slot />
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import DashboardHeader from "@/Components/DashboardHeader.vue";
import DashboardSidepanel from "@/Components/DashboardSidepanel.vue";
export default {
    components: { DashboardHeader, DashboardSidepanel },
    setup() {
        return {};
    },
};
</script>

<style scoped></style>
