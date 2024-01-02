<template>
    <div 
        class="rounded-lg"
        :class="{
            'bg-[#1b1c1c]' : isPrimary,
            'bg-[#34d399]/80' : isSecondary
        }"
    
    >
        <slot></slot>
    </div>
</template>
<script setup>
    const props = defineProps({
        isPrimary: {
            type: Boolean,
            default: false
        },
        isSecondary: {
            type: Boolean,
            default: false
        }
    })
</script>