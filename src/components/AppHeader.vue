<script setup lang="ts">
import { ref } from 'vue'

const isWideHeader = ref(false)

const handleSearchFocus = () => {
  isWideHeader.value = true
}

const handleSearchBlur = () => {
  isWideHeader.value = false
}
</script>

<template>
  <div class="header" :class="{ 'wide': isWideHeader }">
    <!-- 菜单圆圈 -->
    <div class="menu-circle"></div>
    
    <!-- 头部菜单 -->
    <div class="header-menu">
      <a class="menu-link is-active" href="#">应用</a>
      <a class="menu-link notify" href="#">你的工作</a>
      <a class="menu-link" href="#">发现</a>
      <a class="menu-link notify" href="#">市场</a>
    </div>
    
    <!-- 搜索栏 -->
    <div class="search-bar">
      <input 
        type="text" 
        placeholder="搜索" 
        @focus="handleSearchFocus"
        @blur="handleSearchBlur"
      >
    </div>
    
    <!-- 用户信息 -->
    <div class="header-profile">
      <!-- 通知 -->
      <div class="notification">
        <span class="notification-number">3</span>
        <svg viewBox="0 0 24 24" fill="currentColor" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <path d="M18 8A6 6 0 006 8c0 7-3 9-3 9h18s-3-2-3-9M13.73 21a2 2 0 01-3.46 0" />
        </svg>
      </div>
      
      <!-- 云图标 -->
      <svg viewBox="0 0 512 512" fill="currentColor">
        <path d="M448.773 235.551A135.893 135.893 0 00451 211c0-74.443-60.557-135-135-135-47.52 0-91.567 25.313-115.766 65.537-32.666-10.59-66.182-6.049-93.794 12.979-27.612 19.013-44.092 49.116-45.425 82.031C24.716 253.788 0 290.497 0 331c0 7.031 1.703 13.887 3.006 20.537l.015.015C12.719 400.492 56.034 436 106 436h300c57.891 0 106-47.109 106-105 0-40.942-25.053-77.798-63.227-95.449z" />
      </svg>
      
      <!-- 头像 -->
      <img class="profile-img" src="https://images.unsplash.com/photo-1600353068440-6361ef3a86e8?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1000&q=80" alt="用户头像">
    </div>
  </div>
</template>

<style scoped>
.header {
  display: flex;
  align-items: center;
  flex-shrink: 0;
  height: 58px;
  width: 100%;
  border-bottom: 1px solid var(--border-color);
  padding: 0 30px;
  white-space: nowrap;
}

.menu-circle {
  width: 15px;
  height: 15px;
  background-color: #f96057;
  border-radius: 50%;
  box-shadow: 24px 0 0 0 #f8ce52, 48px 0 0 0 #5fcf65;
  margin-right: 195px;
  flex-shrink: 0;
}

.header-menu {
  display: flex;
  align-items: center;
}

.header-menu a {
  padding: 20px 30px;
  text-decoration: none;
  color: var(--inactive-color);
  border-bottom: 2px solid transparent;
  transition: 0.3s;
}

.header-menu a.is-active, .header-menu a:hover {
  color: var(--theme-color);
  border-bottom: 2px solid var(--theme-color);
}

.notify {
  position: relative;
}

.notify:before {
  content: "";
  position: absolute;
  background-color: #3a6df0;
  width: 6px;
  height: 6px;
  border-radius: 50%;
  right: 20px;
  top: 16px;
}

.search-bar {
  height: 40px;
  display: flex;
  width: 100%;
  max-width: 400px;
  padding-left: 16px;
  border-radius: 4px;
}

.search-bar input {
  width: 100%;
  height: 100%;
  border: none;
  background-color: var(--search-bg);
  border-radius: 4px;
  font-family: var(--body-font);
  font-size: 15px;
  font-weight: 500;
  padding: 0 20px 0 40px;
  box-shadow: 0 0 0 2px rgba(134, 140, 160, 0.02);
  background-image: url("data:image/svg+xml;charset=UTF-8,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 56.966 56.966' fill='%23717790c7'%3e%3cpath d='M55.146 51.887L41.588 37.786A22.926 22.926 0 0046.984 23c0-12.682-10.318-23-23-23s-23 10.318-23 23 10.318 23 23 23c4.761 0 9.298-1.436 13.177-4.162l13.661 14.208c.571.593 1.339.92 2.162.92.779 0 1.518-.297 2.079-.837a3.004 3.004 0 00.083-4.242zM23.984 6c9.374 0 17 7.626 17 17s-7.626 17-17 17-17-7.626-17-17 7.626-17 17-17z'/%3e%3c/svg%3e");
  background-size: 14px;
  background-repeat: no-repeat;
  background-position: 16px 48%;
  color: var(--theme-color);
}

.search-bar input::placeholder {
  font-family: var(--body-font);
  color: var(--inactive-color);
  font-size: 15px;
  font-weight: 500;
}

.header-profile {
  display: flex;
  align-items: center;
  padding: 0 16px 0 40px;
  margin-left: auto;
  flex-shrink: 0;
}

.header-profile svg {
  width: 22px;
  color: #f9fafb;
  flex-shrink: 0;
}

.notification {
  position: relative;
}

.notification-number {
  position: absolute;
  background-color: #3a6df0;
  width: 16px;
  height: 16px;
  border-radius: 50%;
  font-size: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
  color: #fff;
  right: -6px;
  top: -6px;
}

.notification + svg {
  margin-left: 22px;
}

.profile-img {
  width: 32px;
  height: 32px;
  border-radius: 50%;
  object-fit: cover;
  border: 2px solid var(--theme-bg-color);
  margin-left: 22px;
}

.wide .header-menu,
.wide .notification {
  display: none;
}

.wide .search-bar {
  max-width: 600px;
  margin-left: 12px;
}

.wide .menu-circle {
  margin-right: 0;
}

@media screen and (max-width: 945px) {
  .menu-circle,
  .notification + svg {
    display: none;
  }
}

@media screen and (max-width: 610px) {
  .header-menu a:not(.is-active) {
    display: none;
  }
}

@media screen and (max-width: 480px) {
  .header {
    padding: 0 16px;
  }
}
</style> 