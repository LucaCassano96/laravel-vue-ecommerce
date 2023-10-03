

<template>
    <div class="min-h-full flex bg-gray-200">

        <!-- Sidebar -->
        <Sidebar :class="{'-ml-[250px]' : !sidebarOpened}"/>


        <div class="flex-1">

            <NavBar @toggle-sidebar="toggleSidebar"/>

            <main class="p-6">
                <router-view></router-view>
            </main>
        </div>
    </div>
</template>

<script setup>

import {ref, onMounted, onUnmounted} from "vue";
import Sidebar from './Sidebar.vue';
import NavBar from './NavBar.vue';

const { title } = defineProps({
    title: String
})

const sidebarOpened = ref (true);

function toggleSidebar(){
    sidebarOpened.value = !sidebarOpened.value
}

onMounted(() => {
    handleSidebarOpened();
    window.addEventListener('resize', handleSidebarOpened)
})

onUnmounted(() =>{
    window.addEventListener('resize', handleSidebarOpened)
})


function handleSidebarOpened(){

    sidebarOpened.value = window.outerWidth > 768;

}

</script>

<style scoped></style>
