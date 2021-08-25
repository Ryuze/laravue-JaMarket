<template>
    <div class="relative bg-green-400">
        <div class="max-w-full mx-auto px-4">
            <div class="flex flex-row justify-between ml-4 mr-4">
                <div class="flex flex-row">
                    <img
                        src="https://vuejs.org/images/logo.svg"
                        alt="logo"
                        class="h-8 w-auto mt-4 mb-4"
                    />
                    <p
                        class="
                            my-auto
                            text-center
                            ml-2
                            text-white text-xl
                            font-bold
                        "
                    >
                        Logo
                    </p>
                </div>
                <div class="my-auto flex flex-row relative">
                    <div>
                        <button
                            type="button"
                            class="
                                inline-flex
                                justify-center
                                w-full
                                rounded-md
                                border border-gray-300
                                shadow-sm
                                px-4
                                py-2
                                bg-white
                                text-sm
                                font-medium
                                text-gray-700
                                hover:bg-gray-50
                                focus:outline-none
                                focus:ring-2
                                focus:ring-offset-2
                                focus:ring-offset-gray-100
                                focus:ring-indigo-500
                            "
                            id="menu-button"
                            aria-expanded="true"
                            aria-haspopup="true"
                        >
                            Options
                            <svg
                                class="-mr-1 ml-2 h-5 w-5"
                                xmlns="http://www.w3.org/2000/svg"
                                viewBox="0 0 20 20"
                                fill="currentColor"
                                aria-hidden="true"
                            >
                                <path
                                    fill-rule="evenodd"
                                    d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
                                    clip-rule="evenodd"
                                />
                            </svg>
                        </button>

                        <!-- TODO: bikin biar ada animasi pas dropdown -->
                        <transition 
                            enter-active-class="transition ease-out duration-100"
                            enter-class="transform opacity-0 scale-95"
                            enter-to-class="transform opacity-100 scale-100"
                            leave-active-class="transition ease-in duration-75"
                            leave-class="transform opacity-100 scale-100"
                            leave-to-class="transform opacity-0 scale-95"
                        >

                        <div
                            class="
                                origin-top-right
                                absolute
                                right-0
                                mt-2
                                w-56
                                rounded-md
                                shadow-lg
                                bg-white
                                ring-1 ring-black ring-opacity-5
                                focus:outline-none
                            "
                            role="menu"
                            aria-orientation="vertical"
                            aria-labelledby="menu-button"
                            tabindex="-1"
                        >
                            <div class="py-1" role="none">
                                <!-- Active: "bg-gray-100 text-gray-900", Not Active: "text-gray-700" -->
                                <a
                                    href="#"
                                    class="
                                        text-gray-700
                                        block
                                        px-4
                                        py-2
                                        text-sm
                                    "
                                    role="menuitem"
                                    tabindex="-1"
                                    id="menu-item-0"
                                    >Account settings</a
                                >
                                <a
                                    href="#"
                                    class="
                                        text-gray-700
                                        block
                                        px-4
                                        py-2
                                        text-sm
                                    "
                                    role="menuitem"
                                    tabindex="-1"
                                    id="menu-item-1"
                                    >Support</a
                                >
                                <a
                                    href="#"
                                    class="
                                        text-gray-700
                                        block
                                        px-4
                                        py-2
                                        text-sm
                                    "
                                    role="menuitem"
                                    tabindex="-1"
                                    id="menu-item-2"
                                    >License</a
                                >
                                <form method="POST" action="#" role="none">
                                    <button
                                        type="submit"
                                        class="
                                            text-gray-700
                                            block
                                            w-full
                                            text-left
                                            px-4
                                            py-2
                                            text-sm
                                        "
                                        role="menuitem"
                                        tabindex="-1"
                                        id="menu-item-3"
                                    >
                                        Sign out
                                    </button>
                                </form>
                            </div>
                        </div>

                        </transition>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    setup() {
        return {};
    },
};
</script>

<style scoped></style>
