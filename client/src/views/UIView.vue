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
      <br>
      <TheAccordion :list="accordionList" :image="accordionImage">
        Клавиатуры
      </TheAccordion>
      <br>
    </main>
  </template>
  <script setup>
  import {ref} from 'vue'
  import TheBlock from "@/components/UI/TheBlock.vue"
  import TheButton from "@/components/UI/TheButton.vue"
  import TheCounter from "@/components/UI/TheCounter.vue"
  import TheAccordion from '@/components/UI/TheAccordion.vue'
  const count = ref(1)
  const accordionList = [
    {
        title: "Featured Keyboards",
        description: "Favourites currently in-stock",
        url: "/"
    },
    {
        title: "Featured Keyboards",
        description: "Favourites currently in-stock",
        url: "/"
    },
    {
        title: "Featured Keyboards",
        description: "Favourites currently in-stock",
        url: "/"
    },
    {
        title: "Featured Keyboards",
        description: "Favourites currently in-stock",
        url: "/"
    },
    {
        title: "Featured Keyboards",
        description: "Favourites currently in-stock",
        url: "/"
    },
    {
        title: "Featured Keyboards",
        description: "Favourites currently in-stock",
        url: "/"
    }
  ]
  const accordionImage = {
    title: "Starter Series",
    name: "https://cdn.shopify.com/s/files/1/0521/7429/1118/files/starterseries-section-head_542x304.png?v=1649339241",
    path: "/keyboards/starter"
  }
  </script>
  