<script setup>
import { ref, onMounted, onUnmounted, computed } from "vue"
import Navbar from "./Navbar.vue"
import Sidebar from "../components/Sidebar.vue"
import Spinner from "./core/Spinner.vue";


import store from "../store";

const {title} = defineProps({
  title: String
  
})

const currentUser = computed(() => store.state.user.data)

const sidebarOpened = ref(true)

function toggleSidebar(){
    console.log('click');
    sidebarOpened.value = !sidebarOpened.value
}
onMounted(() => {
    store.dispatch('getUser')
    handleSidebarOpened()
    window.addEventListener('resize', handleSidebarOpened)
})

onUnmounted(() => {
    window.removeEventListener('resize', handleSidebarOpened)
})

function handleSidebarOpened(){
    if(window.outerWidth <= 768){
        sidebarOpened.value = false
    }else{
        sidebarOpened.value = true
    }
}
</script>

<template>
    <div v-if="currentUser.id" class="min-h-full flex bg-gray-200">
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
    <div v-else class="min-h-full bg-gray-200 flex items-center justify-center">
       <Spinner/>
    </div>


</template>

<style scoped>

</style>
