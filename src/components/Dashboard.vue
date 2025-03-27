<script setup lang="ts">
import { ref } from 'vue'
import SideMenu from './SideMenu.vue'
import AppHeader from './AppHeader.vue'
import MainContent from './MainContent.vue'

const isLightMode = ref(false)
const currentCategory = ref('all')

const toggleLightMode = () => {
  isLightMode.value = !isLightMode.value
  document.body.classList.toggle('light-mode', isLightMode.value)
}

const handleCategoryChange = (category: string) => {
  currentCategory.value = category
}
</script>

<template>
  <div class="bg-image"></div>
  
  <div class="dark-light" @click="toggleLightMode">
    <svg viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5" fill="none" stroke-linecap="round" stroke-linejoin="round">
      <path d="M21 12.79A9 9 0 1111.21 3 7 7 0 0021 12.79z" />
    </svg>
  </div>
  
  <div class="app" :class="{ 'light-mode': isLightMode }">
    <AppHeader />
    <div class="wrapper">
      <SideMenu @category-change="handleCategoryChange" />
      <MainContent :category="currentCategory" />
    </div>
  </div>
</template>

<style scoped>
.app {
  background-color: var(--theme-bg-color);
  max-width: 1600px;
  max-height: 860px;
  height: 90vh;
  display: flex;
  flex-direction: column;
  overflow: hidden;
  position: relative;
  width: 100%;
  border-radius: 14px;
  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(20px);
  font-size: 15px;
  font-weight: 500;
}

.wrapper {
  display: flex;
  flex-grow: 1;
  overflow: hidden;
}

.bg-image {
  position: fixed;
  right: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-image: url('https://images.unsplash.com/22/good-mornin.JPG?auto=format&fit=crop&w=1650');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  z-index: -1;
}

.dark-light {
  position: fixed;
  bottom: 50px;
  right: 30px;
  background-color: var(--dropdown-bg);
  box-shadow: -1px 3px 8px -1px rgba(0, 0, 0, 0.2);
  padding: 8px;
  border-radius: 50%;
  z-index: 3;
  cursor: pointer;
}

.dark-light svg {
  width: 24px;
  flex-shrink: 0;
  fill: #ffce45;
  stroke: #ffce45;
  transition: 0.5s;
}
</style> 