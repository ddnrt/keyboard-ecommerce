<template>
    <div
        class="w-fit rounded-md ease-in duration-200 hover:ring-[#e5e7eb]"
        :class="{
            'bg-white text-black hover:ring-2' : isPrimary,
            'border border-white hover:bg-black hover:ring-2' : isSecondary,
            'bg-black btn_special' : isSpecial }"
    >
        <RouterLink :to="`/` + url" class="block h-full py-4 px-5">
            <slot></slot>
        </RouterLink>
    </div>
</template>
<script setup>
const props = defineProps({
    url: String,
    isPrimary: {
        type: Boolean,
        default: false
    },
    isSecondary: {
        type: Boolean,
        default: false
    },
    isSpecial: {
        type: Boolean,
        default: false
    },
})
</script>
<style scoped>
    a {
        font-weight: 600;
    }
    .btn_special {
        filter: drop-shadow(2px 2px 0 #34d399);
    }
    .btn_special:hover {
        filter: drop-shadow(3px 3px 0 #34d399);
    }
</style>