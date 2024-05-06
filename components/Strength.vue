<template>
    <div>
        <div
            class="max-w-sm bg-white rounded-lg shadow dark:bg-gray-800 dark:border-gray-700 text-center border-green-500 border-[1px] m-auto">
            <a href="#">
                <img class="rounded-t-lg ml-20 p-4" :src="image" alt="" />
            </a>
            <div class="p-5">
                <a href="#">
                    <h5 class="mb-2 text-3xl font-bold tracking-tight text-gray-900 dark:text-white">{{ title }}</h5>
                </a>
                <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">{{ description }}</p>

            </div>
        </div>
    </div>
</template>

<script setup>
defineProps({
    image: "",
    title: "",
    description: ""
})

</script>

<style scoped></style>