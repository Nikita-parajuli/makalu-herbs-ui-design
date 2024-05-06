<template>
    <div>
        <!-- Carousel -->
        <section>
            <Carousel />

        </section>

        <!-- Strength Section -->
        <section>
            <div class="container">
                <h1 class="text-center leading-[54px] font-[700] text-[36px] text-[#05A74F] pt-8">Our Strength</h1>

                <div class="grid grid-cols-4 gap-16 p-10">
                    <Strength :image="`/images/safe.png`" :title="`Safe`"
                        :description="`First WHO GMP Certified Herbal Company of Nepal`" />
                    <Strength :image="`/images/authentic.png`" :title="`Authentic`"
                        :description="`Made with natural herbs of theHimalayan mountains of Nepal`" />
                    <Strength :image="`/images/sceintific.png`" :title="`Scientific`"
                        :description="`Employs the ancient teachings of Ayurvedic Science `" />
                    <Strength :image="`/images/effective.png`" :title="`Effective`"
                        :description="`Heals and nourishes the body with natural properties of herbs`" />

                </div>
            </div>
        </section>

        <!-- commitment section strated -->
        <section>
            <div class="container">
                <h1 class="text-center leading-[54px] font-[700] text-[36px] text-[#05A74F] ">The Makalu Commitments</h1>

                <div class="grid grid-cols-3 gap-20 p-10">
                    <Commitment :image="'/images/wellness.png'" :title="'WELLNESS'" :titles="'Commitment To Wellness'"
                        :description="'To provide cures for all sections of society without compromise on quality.'" />
                    <Commitment :image="'/images/modern.png'" :title="'MODERN & ANCIENT SCIENCE'"
                        :titles="'Commitment To Modern & Ancient Science'"
                        :description="'To pioneer the use of research methodologies of Western Science in conjunction with traditional Ayurvedic formulations.'" />
                    <Commitment :image="'/images/ayurveda.png'" :title="'AYURVEDA'"
                        :titles="'Commitment To Promote Ayurveda'"
                        :description="'To propagate Ayurveda and Ayurvedic cures in an increasingly cosmopolitan world'" />

                </div>
            </div>
        </section>

        <!-- featured section started -->
        <section>
            <div class="container">
                <h1 class="text-center leading-[54px] font-[700] text-[36px] text-[#05A74F] ">Featured Products</h1>

            <div class="flex gap-4 ml-10 r-5px p-4">
                <Featured :image="'/images/calbhas.png'" :title="'Bone & Joint Care'" :description="'Calbhas Tab '"/>
                <Featured :image="'/images/bone.png'" :title="'Bone & Joint Care'" :description="'Calbhas Tab '"/>
                <Featured :image="'/images/boneone.png'" :title="'Bone & Joint Care'" :description="'Calbhas Tab '"/>
                <Featured :image="'/images/bonetwo.png'" :title="'Bone & Joint Care'" :description="'Calbhas Tab '"/>
            </div>
            </div>
        </section>

</div></template>

<script setup>
   
</script>

<style >
</style>