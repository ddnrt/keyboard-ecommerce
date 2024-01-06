<template>
    <div class="md:h-20 bg-black">
        <nav class="flex justify-between mx-40 h-full items-center">
            <div>
                <RouterLink to="/">
                <img src="../assets/logo.png" class="h-14">
                </RouterLink>
            </div>
            <div class="w-2/3 h-full flex items-center">
                <ul class="flex justify-evenly w-full mx-12">
                    <li>
                        <RouterLink to="/catalog">
                            Каталог
                        </RouterLink>
                    </li>
                    <li>
                        <RouterLink to="/catalog">
                            Новинки
                        </RouterLink>
                    </li>
                    <li>
                        <DropdownMenu :list="keyaboardList" :image="keyaboardImage">
                            Клавиатуры
                        </DropdownMenu>
                    </li>
                    <li>
                        <DropdownMenu :list="componentsList" :image="componentsImage">
                            Компоненты
                        </DropdownMenu>
                    </li>
                    <li>
                        <RouterLink to="/catalog">
                            Информация
                        </RouterLink>
                    </li>
                </ul>
            </div>
            <div>
                <ul class="flex w-40 justify-around">
                    <li>
                        <RouterLink to="/catalog">
                            <SearchIcon />
                        </RouterLink>
                    </li>
                    <li>
                        <RouterLink to="/profile">
                            <ProfileIcon />
                        </RouterLink>
                    </li>
                    <li>
                        <RouterLink to="/cart">
                            <CartIcon />
                        </RouterLink>
                    </li>
                </ul>
            </div>

        </nav>
    </div>
</template>
<script setup>
import {RouterLink} from 'vue-router'
import CartIcon from './icons/IconCart.vue'
import SearchIcon from './icons/IconSearch.vue'
import ProfileIcon from './icons/IconProfile.vue'
import DropdownMenu from '@/components/UI/DropdownMenu.vue'

const keyaboardList = [
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
  const keyaboardImage = {
    title: "Starter Series",
    name: "https://cdn.shopify.com/s/files/1/0521/7429/1118/files/starterseries-section-head_542x304.png?v=1649339241",
    path: "/keyboards/starter"
  }
  const componentsList = [
  {
        title: "Switches",
        description: "Favourites currently in-stock",
        url: "/"
    },
    {
        title: "Stabilisers",
        description: "Favourites currently in-stock",
        url: "/"
    },
    {
        title: "Keycaps",
        description: "Favourites currently in-stock",
        url: "/"
    },
    {
        title: "Barebones Kits",
        description: "Favourites currently in-stock",
        url: "/"
    },
    {
        title: "Coiled Cables",
        description: "Favourites currently in-stock",
        url: "/"
    },
    {
        title: "Accessories and Tools",
        description: "Favourites currently in-stock",
        url: "/"
    }
  ]
  const componentsImage = {
    title: "Shoko Keycaps",
    name: "https://landingpad.shop/cdn/shop/products/shoko.jpg",
    path: "/components/keycaps/shoko"
  }
</script>