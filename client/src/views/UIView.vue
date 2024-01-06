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
      <DropdownMenu :list="dropdownList" :image="dropdownImage">
        Клавиатуры
      </DropdownMenu>
      <br>
    </main>
  </template>
  <script setup>
  import {ref} from 'vue'
  import TheBlock from "@/components/UI/TheBlock.vue"
  import TheButton from "@/components/UI/TheButton.vue"
  import TheCounter from "@/components/UI/TheCounter.vue"
  import DropdownMenu from '@/components/UI/DropdownMenu.vue'
  const count = ref(1)
  const dropdownList = [
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
  const dropdownImage = {
    title: "Starter Series",
    name: "https://cdn.shopify.com/s/files/1/0521/7429/1118/files/starterseries-section-head_542x304.png?v=1649339241",
    path: "/keyboards/starter"
  }
  </script>
  