<script setup>
import Sidebar from "../components/Sidebar.vue"
import Navbar from "./Navbar.vue";

const {title} = defineProps({
  title: String
  
})
</script>

<template>
    <div class="min-h-full flex bg-gray-200">
        <!-- sidebar -->
        <Sidebar />
        <div class="flex-1">
            <Navbar/>

            <!-- content -->
            <main class="p-6">
            <router-view></router-view>
            </main>

        </div>
      
    </div>


</template>

<style scoped>

</style>
