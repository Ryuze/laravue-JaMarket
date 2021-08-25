<template>
    <Head title="Create Product" />
    <div class="flex h-screen">
        <div class="m-auto">
            <form @submit.prevent="store()">
                <div>
                    <label for="name" class="block font-bold"
                        >Product name</label
                    >
                    <input
                        type="text"
                        id="name"
                        class="
                            shadow
                            border
                            rounded-md
                            w-full
                            py-2
                            px-3
                            border-gray-300
                            focus:outline-none
                            focus:ring-0
                            focus:border-green-400
                        "
                        v-model="product.name"
                    />
                    <div class="text-red-600">Validation Message</div>
                </div>
                <div>
                    <label for="price" class="block font-bold"
                        >Product price</label
                    >
                    <input
                        type="number"
                        id="price"
                        class="
                            shadow
                            border
                            rounded-md
                            w-full
                            py-2
                            px-3
                            border-gray-300
                            focus:outline-none
                            focus:ring-0
                            focus:border-green-400
                        "
                        v-model="product.price"
                    />
                    <div class="text-red-600">Validation Message</div>
                </div>
                <div>
                    <button
                        type="submit"
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
                        Create
                    </button>
                </div>
            </form>
        </div>
    </div>
</template>

<script>
import { Head, Link } from "@inertiajs/inertia-vue3";
import { reactive, ref } from "vue";
import axios from "axios";

export default {
    components: {
        Head,
        Link,
    },
    setup() {
        const product = reactive({
            name: "",
            price: "",
        });

        const validation = ref([]);

        // TODO: selesai add data harusnya balik ke index tpi jangan sampe refresh
        function store() {
            axios
                .post(route("product.store"), product)
                .then(() => {
                    window.open(route("index"), "_self");
                })
                .catch((err) => {
                    validation.value = err.response.data;
                });
        }

        return {
            product,
            validation,
            store,
        };
    },
};
</script>

<style scoped></style>
