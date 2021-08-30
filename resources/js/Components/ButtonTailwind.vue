<template>
    <button
        :type="type"
        class="
            border
            rounded
            shadow-sm
            items-center
            transition
            ease-in-out
            duration-150
            text-white
            font-bold
            px-4
            py-2
        "
    >
        <slot />
    </button>
</template>

<script>
export default {
    setup() {
        return {};
    },
    props: {
        type: {
            type: String,
            default: "submit",
        },
    },
};
</script>
