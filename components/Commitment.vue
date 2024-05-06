<template>
    <div>
        
<div class="max-w-sm border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700 h-[461.89px] w-[442px] bg-[#E7FFF2]">
    <a href="#">
        <img class="rounded-t-lg w-[429.28px] h-[290.46px]" :src="image" alt="" />
    </a>
    <div class="p-5">
        <a href="#">
            <h3 class="font-[600] text-[#05A74F] Leading-[24px] text-[14px]">{{ title }}</h3>
            <h5 class="mb-2 text-[16px] leading-[27px] tracking-tight text-gray-900 dark:text-white font-[700]">{{ titles }}</h5>
        </a>
        <p class="mb-3 text-gray-700 dark:text-gray-400 leading-[20px] font-[400] text-[16px]">{{ description }}</p>
       
    </div>
</div>


    </div>
</template>

<script setup>
 defineProps({
        image: "",
        title: "",
        titles: "",
        description: ""
    })

</script>

<style scoped>

</style>