<script setup>
import { computed } from '@vue/reactivity';
import { useRouter } from 'vue-router';

import IconSearch from './components/icons/IconSearch.vue'

const logoSize = 'width:85px;';
const myRouter = useRouter()
const goToHome = () => myRouter.push({ name: 'Home' })
const goToContact = () => myRouter.push({ name: 'ContactUs' })
const goToWishlist = () => myRouter.push({ name: 'Wishlist' })




</script>
 
<template>
    <div>
        <div>
            <!-- navbar goes here -->
            <nav class="bg-white drop-shadow-md rounded-lg ">
                <div class="max-w-screen-xl mx-auto px-4 my-">
                    <div class="flex justify-between">
                        <div class="flex space-x-4">
                            <!-- logo -->
                            <div>
                                <a href="#" class="flex items-center py-5 px-2 text-gray-700 hover:text-gray-900"
                                    @click="goToHome">
                                    <img src="./assets/FUNBOOK-LOGO.png" alt="LOGO" :style="logoSize" />
                                    <span class="font-bold text-xl">FUNBOOK<br><span class=" font-light">online book
                                            store</span></span>

                                </a>
                            </div>
                        </div>
                        


                        <!-- secondary nav -->
                        <div class="hidden md:flex items-center space-x-1">
                            <button type="button" class="inline-block px-6 py-2.5 bg-blue-400 text-white 
                            font-medium text-xs leading-tight uppercase rounded 
                            shadow-sm hover:bg-blue-500 hover:shadow-lg focus:bg-blue-500
                            focus:shadow-lg focus:outline-none focus:ring-0 active:bg-blue-600
                            active:shadow-lg transition duration-150 ease-in-out" @click="goToHome">HOME</button>


                            <button type="button" class="inline-block px-6 py-2.5 bg-gray-200 text-gray-700
                            font-medium text-xs leading-tight uppercase rounded 
                            shadow-sm hover:bg-gray-300 hover:shadow-lg focus:bg-gray-300 
                            focus:shadow-lg focus:outline-none focus:ring-0 active:bg-gray-400
                            active:shadow-lg transition duration-150 ease-in-out"
                                @click="goToWishlist">WISHLIST</button>

                            <button type="button" class="inline-block px-6 py-2.5 bg-gray-800 text-white 
                            font-medium text-xs leading-tight uppercase rounded shadow-sm 
                            hover:bg-gray-900 hover:shadow-lg focus:bg-gray-900 focus:shadow-lg 
                            focus:outline-none focus:ring-0 active:bg-gray-900 active:shadow-lg 
                            transition duration-150 ease-in-out" @click="goToContact">CONTACT US</button>
                        </div>
                    </div>
                </div>
            </nav>
            <router-view />
        </div>
    </div>
</template>
 
<style>
</style>