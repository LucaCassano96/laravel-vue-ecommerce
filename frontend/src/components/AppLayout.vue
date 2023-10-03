

<template>
    <div class="min-h-full flex bg-gray-200">

        <!-- Sidebar -->
        <Sidebar :class="{'-ml-[250px]' : !sidebarOpened}"/>


        <div class="flex-1">

            <TopHeader @toggle-sidebar="toggleSidebar"/>

            <main class="p-6">
                <router-view></router-view>
            </main>
        </div>
    </div>
</template>

<script setup>

import {ref} from "vue";
import Sidebar from './Sidebar.vue';
import TopHeader from './TopHeader.vue';

const { title } = defineProps({
    title: String
})

const sidebarOpened = ref (true);

function toggleSidebar(){
    sidebarOpened.value = !sidebarOpened.value
}


</script>

<style scoped></style>
