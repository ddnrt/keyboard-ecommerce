<template>
  <main>
    <h2>Custom Keyboards for everyone</h2>
    <p>Checkout with Shopback for up to $25 off</p>
    <br>
    <TheBlock  class="w-100 h-40" />
    <br>
    <TheButton url="1" :isPrimary="true">Need help?</TheButton>
    <br>
    <TheButton url="2" :isSecondary="true">Try out keyboards</TheButton>
    <br>
    <TheButton url="3" :isSpecial="true">Build Keyboard</TheButton>
  </main>
</template>
<script setup>
import TheBlock from "../components/UI/TheBlock.vue"
import TheButton from "../components/UI/TheButton.vue"
</script>
