<script setup lang="ts">
interface Props {
  title: string
  subtext: string
  icon: string
}

defineProps<Props>()
</script>

<template>
  <div class="app-card">
    <span>
      <svg viewBox="0 0 52 52" style="border:1px solid #c1316d">
        <g xmlns="http://www.w3.org/2000/svg">
          <path d="M40.824 52H11.176C5.003 52 0 46.997 0 40.824V11.176C0 5.003 5.003 0 11.176 0h29.649C46.997 0 52 5.003 52 11.176v29.649C52 46.997 46.997 52 40.824 52z" fill="#2f0015" data-original="#393687" />
          <path d="M30.68 39h-3.24l-2.76-9.04h-8.32L13.72 39H10.6l8.24-28h3.32l8.52 28zm-6.72-12l-3.48-11.36L17.12 27h6.84z" fill="#e7adfb" data-original="#89d3ff" />
        </g>
      </svg>
      <img :src="icon" alt="App icon">
    </span>
    <div class="app-card__content">
      <div class="app-card__title">{{ title }}</div>
      <div class="app-card__subtext">{{ subtext }}</div>
      <div class="app-card-buttons">
        <button class="content-button status-button">更新</button>
        <div class="menu"></div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.app-card {
  width: calc(33.3% - 20px);
  font-size: 16px;
  background-color: var(--content-bg);
  border-radius: 14px;
  border: 1px solid var(--border-color);
  padding: 20px;
  cursor: pointer;
  transition: 0.3s ease;
  margin: 10px;
}

.app-card:hover {
  transform: scale(1.02);
  background-color: var(--theme-bg-color);
}

.app-card span {
  display: flex;
  align-items: center;
}

.app-card svg {
  width: 28px;
  border-radius: 6px;
  margin-right: 12px;
  flex-shrink: 0;
}

.app-card span img {
  width: 28px;
  border-radius: 6px;
  margin-left: 12px;
  flex-shrink: 0;
}

.app-card__title {
  font-weight: 500;
  color: var(--theme-color);
  margin-top: 12px;
}

.app-card__subtext {
  font-size: 14px;
  font-weight: 400;
  line-height: 1.6em;
  color: var(--inactive-color);
  margin-top: 8px;
}

.app-card-buttons {
  display: flex;
  align-items: center;
  margin-left: auto;
  margin-top: 16px;
}

@media screen and (max-width: 1110px) {
  .app-card {
    width: calc(50% - 20px);
  }
}

@media screen and (max-width: 565px) {
  .app-card {
    width: calc(100% - 20px);
  }
}
</style> 