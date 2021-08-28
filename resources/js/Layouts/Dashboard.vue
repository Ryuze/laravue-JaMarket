<template>
    <div id="navigation" class="static">
        <div class="fixed top-0 left-0 right-0">
            <dashboard-header />
            <div class="fixed left-0 hidden md:block">
                <dashboard-sidepanel />
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
