<script setup>
import { HomeIcon,UsersIcon, ShoppingBagIcon, ChartBarIcon } from "@heroicons/vue/24/outline"

</script>

<template>
    <div class="w-[200px] transition-all bg-indigo-700 text-gray-200 md:text-lg py-4 px-2">
  
       <router-link :to="{name: 'app.dashboard'}" class="flex items-center hover:bg-black/30 py-2 px-3 rounded transition-colors mb-2">
          <span class="mr-5"><HomeIcon class="w-5"/></span>
          <span >Dashboard</span>
       </router-link>
  
       <!-- <router-link :to="{name: 'app.products'}" class="flex items-center hover:bg-black/30 py-2 px-3 rounded transition-colors mb-2">
          <span class="mr-5"><ShoppingBagIcon class="w-5"/></span>
          <span>Products</span>
       </router-link> -->
<!--   
       <router-link :to="{name: 'app.dashboard'}" class="flex items-center hover:bg-black/30 py-2 px-3 rounded transition-colors mb-2">
          <span class="mr-5"><UsersIcon class="w-5"/></span>
          <span>Users</span>
       </router-link> -->
  
       <!-- <router-link :to="{name: 'app.dashboard'}" class="flex items-center hover:bg-black/30 py-2 px-3 rounded transition-colors mb-2">
          <span class="mr-5"><ChartBarIcon class="w-5"/></span>
          <span>Reports</span>
       </router-link> -->
  
      </div>
</template>
  
