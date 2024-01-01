<script setup>
import {RouterLink} from 'vue-router'
import CartIcon from './icons/IconCart.vue'
import SearchIcon from './icons/IconSearch.vue'
import ProfileIcon from './icons/IconProfile.vue'
</script>

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
                        <RouterLink to="/catalog">
                            Клавиатуры
                        </RouterLink>
                    </li>
                    <li>
                        <RouterLink to="/catalog">
                            Компоненты
                        </RouterLink>
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
