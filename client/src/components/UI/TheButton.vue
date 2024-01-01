<template>
    <div
        class="w-fit rounded-md"
        :class="{
            'bg-white text-black' : isPrimary,
            'bg-black border border-white' : isSecondary,
            '' : isMain }"
    >
        <RouterLink :to="`/` + url" class="block h-full py-3 px-2">
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
</style>