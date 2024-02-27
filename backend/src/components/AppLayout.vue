<script setup>
import { ref } from "vue";
import Sidebar from "../components/Sidebar.vue"
import Navbar from "./Navbar.vue";

const {title} = defineProps({
  title: String
  
})

const sidebarOpened = ref(true)

function toggleSidebar(){
    console.log('click');
    sidebarOpened.value = !sidebarOpened.value
}
</script>

<template>
    <div class="min-h-full flex bg-gray-200">
        <!-- sidebar -->
        <Sidebar :class="{'-ml-[200px]' : !sidebarOpened}"/>
        <div class="flex-1">
            <Navbar @toggle-sidebar="toggleSidebar"/>

            <!-- content -->
            <main class="p-6">
            <router-view></router-view>
            </main>

        </div>
      
    </div>


</template>

<style scoped>

</style>
