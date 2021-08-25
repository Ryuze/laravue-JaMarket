<template>
    <Head title="Homepage" />
    <div class="flex h-screen">
        <p class="text-center m-auto font-extrabold">
            Homepage disini
            <Link
                :href="route('product.create')"
                class="
                    bg-green-500
                    hover:bg-green-700
                    text-white
                    font-bold
                    py-2
                    px-4
                    rounded
                "
            >
                Tambah produk
            </Link>
        </p>
        <div>
            <p class="m-auto">
                <Link
                    :href="route('login')"
                    class="
                        bg-green-500
                        text-white
                        font-bold
                        py-2
                        px-4
                        rounded
                        hover:bg-green-700
                    "
                >
                    Login
                </Link>
                <Link
                    :href="route('register')"
                    class="
                        bg-green-500
                        text-white
                        font-bold
                        py-2
                        px-4
                        rounded
                        hover:bg-green-700
                    "
                >
                    Register
                </Link>
            </p>
        </div>
    </div>
</template>

<script>
import { Head, Link } from "@inertiajs/inertia-vue3";
import axios from "axios";
import { onMounted, ref } from "vue";

export default {
    components: {
        Head,
        Link,
    },
};
</script>

<style scoped></style>
