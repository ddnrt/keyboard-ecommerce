<template>
    <main>
      <h2>Custom Keyboards for everyone</h2>
      <p>Checkout with Shopback for up to $25 off</p>
      <br>
      <TheBlock  class="w-100 h-40" isSecondary="true" />
      <br>
      <TheBlock  class="w-100 h-40" isPrimary="true" />
      <br>
      <TheButton url="1" :isPrimary="true">Need help?</TheButton>
      <br>
      <TheButton url="2" :isSecondary="true">Try out keyboards</TheButton>
      <br>
      <TheButton url="3" :isSpecial="true">Build Keyboard</TheButton>
      <br>
      <div>
        <h2>{{ count }}</h2>
        <TheCounter v-model:count="count" />  
      </div>
    </main>
  </template>
  <script setup>
  import {ref} from 'vue'
  import TheBlock from "../components/UI/TheBlock.vue"
  import TheButton from "../components/UI/TheButton.vue"
  import TheCounter from "../components/UI/TheCounter.vue"
  const count = ref(1)
  </script>
  