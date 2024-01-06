<template>
    <div>
        <button @click="isOpen = !isOpen" class="flex items-center gap-2">
            <slot></slot>
            <AccordionIcon class="w-3 h-3" />
        </button>
    </div>
    <Transition>
        <div 
            v-if="isOpen"
            class="px-5 py-5 bg-black w-1/2 flex h-[17rem] gap-6 border border-white/60 rounded-md" 
        >
            <ul class="w-2/3 grid grid-rows-3 grid-cols-2 gap-3">
                <li v-for="item in list.slice(0, 6)" class="my-2 mx-1">
                    <RouterLink to="item.url" class="grid grid-rows-2 items-center h-full hover:bg-gray-800 rounded-md ease-in duration-200 p-1">
                        <p class="hover:text-white ease-in duration-200">{{item.title}}</p>
                        <span class="text-sm">{{item.description}}</span>
                    </RouterLink>
                </li>
            </ul>
            <div class="w-1/3 relative">
                <RouterLink :to="image.path">
                    <div class="absolute top-0 inset-x-0 z-10 text-center hover:opacity-0 transition-opacity duration-500 bg-gradient-to-b from-cyan-700/90">
                        <div class="mt-4 mb-16">
                                <div class="text-xl font-semibold text-white">{{ image.title }}</div>
                        </div>
                    </div>
                    <img :src="image.name" class="h-full object-cover rounded-md">
                </RouterLink>
            </div>
        </div>
    </Transition>
</template>
<script setup>
import AccordionIcon from '../icons/IconAccordion.vue'
import { RouterLink } from 'vue-router';
import {ref} from 'vue';
const isOpen = ref(false)
const props = defineProps({
    list: {
        type: Array
    },
    image: {
        type: Object
    }
})
</script>
<style scoped>
    .v-enter-active,
    .v-leave-active {
    transition: opacity 0.2s ease;
    }

    .v-enter-from,
    .v-leave-to {
    opacity: 0;
    }
</style>