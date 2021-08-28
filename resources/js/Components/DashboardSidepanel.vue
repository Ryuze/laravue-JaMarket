<template>
    <div
        class="
            flex flex-col
            bg-black bg-opacity-85
            text-white
            w-screen
            max-w-16
            h-screen
        "
    >
        <div class="bg-black bg-opacity-50 border border-black">
            <img
                src="https://randomuser.me/api/portraits/men/76.jpg"
                alt="photo-profile"
                class="rounded-full h-12 w-12 items-center mx-auto m-2"
            />
            <p class="text-center font-bold mb-2">Jermain Johns</p>
        </div>
        <div class="mb-4">
            <p class="text-gray-500 font-bold text-xs mb-1 ml-4 mt-2 mr-4">
                PRODUCTIONS
            </p>
            <ul>
                <li
                    class="
                        text-gray-400 text-lg
                        font-bold
                        border-0
                        rounded-md
                        hover:bg-gray-500 hover:text-gray-100
                    "
                >
                    <Link :href="route('dashboard.product')">
                        <p class="ml-4 py-1">
                            <i class="bi bi-basket pr-1"></i> Products
                        </p>
                    </Link>
                </li>
                <li
                    class="
                        text-gray-400 text-lg
                        font-bold
                        border-0
                        rounded-md
                        hover:bg-gray-500 hover:text-gray-100
                    "
                >
                    <Link href="/dashboard/category">
                        <p class="ml-4 py-1">
                            <i class="bi bi-bookmarks pr-1"></i> Categories
                        </p>
                    </Link>
                </li>
            </ul>
        </div>
        <div class="mb-4">
            <p class="text-gray-500 font-bold text-xs mb-1 ml-4 mt-2 mr-4">
                MANAGEMENTS
            </p>
            <ul>
                <li
                    class="
                        text-gray-400 text-lg
                        font-bold
                        border-0
                        rounded-md
                        hover:bg-gray-500 hover:text-gray-100
                    "
                >
                    <Link href="/dashboard/user">
                        <p class="ml-4 py-1">
                            <i class="bi bi-people pl-1"></i> Users
                        </p>
                    </Link>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
import { Link } from "@inertiajs/inertia-vue3";

export default {
    setup() {
        return {};
    },
    components: {
        Link,
    },
};
</script>

<style scoped></style>
