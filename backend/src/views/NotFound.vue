<script setup>

</script>

<template>
    <div class="flex items-center justify-center min-h-full min-w-full select-none">
       <div class="flex bg-white p-36 rounded-md">
        <div class="text-indigo-600 text-6xl font-bold px-8 border-r pb-8 ">404</div>
        <div class="px-8">
            <h1 class="text-5xl font-bold mb-2">Page Not Found</h1>
            <p class="text-gray-400 mb-8">Please check the url in address bar and try again.</p>
            <div>
                <router-link :to="{name: 'app.dashboard'}" class=" rounded-md bg-indigo-600 px-6 py-3 text-sm font-semibold leading-6 text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">Go back home</router-link>
            </div>
        </div>
       </div>
    </div>
</template>

<style scoped>

</style>
