
<template>
    <!-- Sidebar -->
    <div class="w-[250px] transition-all bg-indigo-600 rounded-br-xl text-gray-100 py-5 px-3">

        <router-link class="flex items-center rounded transition-colors hover:bg-black/30 p-3 px-2"
            :to="{ name: 'app.dashboard' }">

            <span class="mr-2">
                <HomeIcon class="w-6" />
            </span>
            <span class="text-lg font-light">
                Dashboard
            </span>
        </router-link>

        <router-link class="flex items-center rounded transition-colors hover:bg-black/30 p-3 px-2"
            :to="{ name: 'app.products' }">

            <span class="mr-2">
                <ShoppingCartIcon class="w-6" />
            </span>
            <span class="text-lg font-light">
                Products
            </span>
        </router-link>

        <router-link class="flex items-center rounded transition-colors hover:bg-black/30 p-3 px-2"
            :to="{ name: 'app.dashboard' }">

            <span class="mr-2">
                <UserIcon class="w-6" />
            </span>
            <span class="text-lg font-light">
                Users
            </span>
        </router-link>

        <router-link class="flex items-center rounded transition-colors hover:bg-black/30 p-3 px-2"
            :to="{ name: 'app.dashboard' }">

            <span class="mr-2">
                <ChartPieIcon class="w-6" />
            </span>
            <span class="text-lg font-light">
                Reports
            </span>
        </router-link>

    </div>
</template>

<script setup>
import { HomeIcon, ShoppingCartIcon, UserIcon, ChartPieIcon } from '@heroicons/vue/24/outline';
</script>


