<template>
    <div class="border border-white/80 flex w-[150px] h-10">
        <button @click="reduce" class="block w-1/3">-</button>
        <input
            min='1'
            v-model="count"
            type="number"
            name="count"
            class="appearance-none block w-1/3 bg-transparent text-center text-white"
        >
        <button @click="add" class="block w-1/3">+</button>
    </div>
</template>
<script setup>
const count = defineModel('count')
function reduce() {
    if (count.value > 0) {
        count.value--
    }
}
function add() {
    count.value++
}
</script>