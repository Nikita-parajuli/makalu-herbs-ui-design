<template>
    <div class="relative max-h-[600px] flex flex-col w-full aspect-[4/3] gap-1">
      <SfScrollable
        class="w-full h-full snap-x snap-mandatory [&::-webkit-scrollbar]:hidden [-ms-overflow-style:none] [scrollbar-width:none]"
        :active-index="activeIndex"
        wrapper-class="h-full group/scrollable"
        is-active-index-centered
        :previous-disabled="activeIndex === 0"
        :next-disabled="activeIndex === images.length - 1"
        buttons-placement="block"
        @on-prev="activeIndex -= 1"
        @on-next="activeIndex += 1"
      >
        <!-- Previous Button -->
        <template #previousButton="defaultProps">
          <SfButton
            v-bind="defaultProps"
            :disabled="activeIndex === 0"
            class="absolute hidden group-hover/scrollable:block disabled:!hidden !rounded-full !p-3 z-10 top-1/2 left-4 bg-white"
            variant="secondary"
            size="lg"
            square
          >
            <SfIconChevronLeft />
          </SfButton>
        </template>
  
        <!-- Images -->
        <div v-for="(image, index) in images" :key="index" class="relative flex justify-center basis-full snap-center snap-always shrink-0 grow">
          <img
            class="object-cover w-auto h-full"
            :aria-label="image.alt"
            :aria-hidden="activeIndex !== index"
            :alt="image.alt"
            :src="image.imageSrc"
            draggable="false"
          />
        </div>
  
        <!-- Next Button -->
        <template #nextButton="defaultProps">
          <SfButton
            v-bind="defaultProps"
            :disabled="activeIndex === images.length - 1"
            class="absolute hidden group-hover/scrollable:block disabled:!hidden !rounded-full !p-3 z-10 top-1/2 right-4 bg-white"
            variant="secondary"
            size="lg"
            square
          >
            <SfIconChevronRight />
          </SfButton>
        </template>
      </SfScrollable>
  
      <!-- Image Navigation Bullets -->
      <div class="flex-shrink-0 basis-auto">
        <div class="flex-row w-full flex gap-0.5 mt [&::-webkit-scrollbar]:hidden [-ms-overflow-style:none] [scrollbar-width:none]">
          <button
            v-for="(image, index) in images"
            :key="`${index}-bullet`"
            :aria-current="activeIndex === index"
            :aria-label="image.alt"
            :class="[
              'w-full relative mt-1 border-b-4 transition-colors focus-visible:outline focus-visible:outline-offset-0 pointer-events-none',
              activeIndex === index ? 'border-primary-700' : 'border-gray-200',
            ]"
            @click="activeIndex = index"
          />
        </div>
      </div>
    </div>
  </template>
  
  
<script lang="ts" setup>
import { SfScrollable, SfButton, SfIconChevronLeft, SfIconChevronRight } from '@storefront-ui/vue';
import { ref } from 'vue';

const withBase = (filepath: string) => `/images/${filepath}`;

const activeIndex = ref(0);

// Computed property to generate image data for carousel.png
const images = [
  { imageSrc: withBase('carousel.png'), alt: 'carousel' },
  { imageSrc: withBase('carousel.png'), alt: 'carousel' },
  { imageSrc: withBase('carousel.png'), alt: 'carousel' },
];
</script>

  