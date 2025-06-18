<template>
  <div>
    <nav class="bg-gray-800 text-white p-4 space-x-4">
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
      <router-link to="/contact">Contact</router-link>
    </nav>
    <router-view />
  </div>
</template>
