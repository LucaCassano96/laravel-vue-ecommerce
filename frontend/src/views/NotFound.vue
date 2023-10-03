<template>
    <div class="flex justify-center items-center w-full min-h-full min-w-full">
        <div class="text-indigo-600 text-5xl px-8 font-bold border-r">404</div>
        <div class="px-8">
            <h1 class="text-5xl font-bold mb-4">Page Not Found</h1>
            <p class="text-gray-500  mb-8">please check the url in address bar and try again</p>
            <div>
                <router-link :to="{name: 'app.dashboard'}" class="mt-8 py-2 px-4 border border-transparent text-sm font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500">Go back home
                </router-link>
            </div>
        </div>
    </div>
</template>



<script setup>




</script>
