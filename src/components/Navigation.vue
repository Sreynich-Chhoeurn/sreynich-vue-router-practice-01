<template>
  <nav class="h-16 flex w-10/12 m-auto  items-center justify-between">
    <div id="nav-item" class="flex items-center gap-12">
      <navigation-item 
      v-for="item in navItems" 
      :key="item.label" 
      :item="item"
      :to="item.path">
    </navigation-item>
    
    </div>
    <div id="nav-item" class="flex items-center m-auto gap-12">
        <navigation-item :item="{label:'Login', path: '/login', icon: 'login'}"></navigation-item>
    </div>
  </nav>
</template>

<script setup>
import NavigationItem from "./NavigationItem.vue";
import { ref } from "vue";

const navItems = ref([
  { path: '/', name: 'home', component: Home },
  { label: "About", path: "/about", icon: "menu_book" },
  { label: "Contact", path: "/contact", icon: "shopping_cart_checkout" },
]);
</script>

<style lang="scss" scoped>
</style>