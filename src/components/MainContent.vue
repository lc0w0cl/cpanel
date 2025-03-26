<script setup lang="ts">
import { ref } from 'vue'
import AppCard from './AppCard.vue'
</script>

<template>
  <div class="main-container">
    <!-- 主头部 -->
    <div class="main-header">
      <a class="menu-link-main" href="#">所有应用</a>
      <div class="header-menu">
        <a class="main-header-link is-active" href="#">桌面端</a>
        <a class="main-header-link" href="#">移动端</a>
        <a class="main-header-link" href="#">网页端</a>
      </div>
    </div>
    
    <!-- 内容区域 -->
    <div class="content-wrapper">
      <!-- 头部卡片 -->
      <div class="content-wrapper-header">
        <div class="content-wrapper-context">
          <h3 class="img-content">
            <svg viewBox="0 0 512 512">
              <path d="M467 0H45C20.099 0 0 20.099 0 45v422c0 24.901 20.099 45 45 45h422c24.901 0 45-20.099 45-45V45c0-24.901-20.099-45-45-45z" fill="#d6355b" data-original="#ff468c" />
              <path xmlns="http://www.w3.org/2000/svg" d="M512 45v422c0 24.901-20.099 45-45 45H256V0h211c24.901 0 45 20.099 45 45z" fill="#d6355b" data-original="#d72878" />
              <path xmlns="http://www.w3.org/2000/svg" d="M467 30H45c-8.401 0-15 6.599-15 15v422c0 8.401 6.599 15 15 15h422c8.401 0 15-6.599 15-15V45c0-8.401-6.599-15-15-15z" fill="#2e000a" data-original="#700029" />
              <path xmlns="http://www.w3.org/2000/svg" d="M482 45v422c0 8.401-6.599 15-15 15H256V30h211c8.401 0 15 6.599 15 15z" fill="#2e000a" data-original="#4d0e06" />
              <path xmlns="http://www.w3.org/2000/svg" d="M181 391c-41.353 0-75-33.647-75-75 0-8.291 6.709-15 15-15s15 6.709 15 15c0 24.814 20.186 45 45 45s45-20.186 45-45-20.186-45-45-45c-41.353 0-75-33.647-75-75s33.647-75 75-75 75 33.647 75 75c0 8.291-6.709 15-15 15s-15-6.709-15-15c0-24.814-20.186-45-45-45s-45 20.186-45 45 20.186 45 45 45c41.353 0 75 33.647 75 75s-33.647 75-75 75z" fill="#d6355b" data-original="#ff468c" />
              <path xmlns="http://www.w3.org/2000/svg" d="M391 361h-30c-8.276 0-15-6.724-15-15V211h45c8.291 0 15-6.709 15-15s-6.709-15-15-15h-45v-45c0-8.291-6.709-15-15-15s-15 6.709-15 15v45h-15c-8.291 0-15 6.709-15 15s6.709 15 15 15h15v135c0 24.814 20.186 45 45 45h30c8.291 0 15-6.709 15-15s-6.709-15-15-15z" fill="#d6355b" data-original="#d72878" />
            </svg>
            Adobe Stock
          </h3>
          <div class="content-text">注册Adobe Stock 30天免费试用计划，获取10张免费图片，为您的新项目找到完美图片。</div>
          <button class="content-button">开始免费试用</button>
        </div>
        <img class="content-wrapper-img" src="https://assets.codepen.io/3364143/glass.png" alt="">
      </div>
      
      <!-- 已安装应用部分 -->
      <div class="content-section">
        <div class="content-section-title">已安装</div>
        <ul>
          <!-- Photoshop -->
          <li class="adobe-product">
            <div class="products">
              <svg viewBox="0 0 52 52" style="border:1px solid #3291b8">
                <g xmlns="http://www.w3.org/2000/svg">
                  <path d="M40.824 52H11.176C5.003 52 0 46.997 0 40.824V11.176C0 5.003 5.003 0 11.176 0h29.649C46.997 0 52 5.003 52 11.176v29.649C52 46.997 46.997 52 40.824 52z" fill="#061e26" data-original="#393687" />
                  <path d="M12.16 39H9.28V11h9.64c2.613 0 4.553.813 5.82 2.44 1.266 1.626 1.9 3.76 1.9 6.399 0 .934-.027 1.74-.08 2.42-.054.681-.22 1.534-.5 2.561-.28 1.026-.66 1.866-1.14 2.52-.48.654-1.213 1.227-2.2 1.72-.987.494-2.16.74-3.52.74h-7.04V39zm0-12h6.68c.96 0 1.773-.187 2.44-.56.666-.374 1.153-.773 1.46-1.2.306-.427.546-1.04.72-1.84.173-.801.267-1.4.28-1.801.013-.399.02-.973.02-1.72 0-4.053-1.694-6.08-5.08-6.08h-6.52V27zM29.48 33.92l2.8-.12c.106.987.6 1.754 1.48 2.3.88.547 1.893.82 3.04.82s2.14-.26 2.98-.78c.84-.52 1.26-1.266 1.26-2.239s-.36-1.747-1.08-2.32c-.72-.573-1.6-1.026-2.64-1.36-1.04-.333-2.086-.686-3.14-1.06a7.36 7.36 0 01-2.78-1.76c-.987-.934-1.48-2.073-1.48-3.42s.54-2.601 1.62-3.761 2.833-1.739 5.26-1.739c.854 0 1.653.1 2.4.3.746.2 1.28.394 1.6.58l.48.279-.92 2.521c-.854-.666-1.974-1-3.36-1-1.387 0-2.42.26-3.1.78-.68.52-1.02 1.18-1.02 1.979 0 .88.426 1.574 1.28 2.08.853.507 1.813.934 2.88 1.28 1.066.347 2.126.733 3.18 1.16 1.053.427 1.946 1.094 2.68 2s1.1 2.106 1.1 3.6c0 1.494-.6 2.794-1.8 3.9-1.2 1.106-2.954 1.66-5.26 1.66-2.307 0-4.114-.547-5.42-1.64-1.307-1.093-1.987-2.44-2.04-4.04z" fill="#c1dbe6" data-original="#89d3ff" />
                </g>
              </svg>
              Photoshop
            </div>
            <span class="status">
              <span class="status-circle green"></span>
              已更新
            </span>
            <div class="button-wrapper">
              <button class="content-button status-button open">打开</button>
              <div class="menu">
                <button class="dropdown">
                  <ul>
                    <li><a href="#">前往发现</a></li>
                    <li><a href="#">了解更多</a></li>
                    <li><a href="#">卸载</a></li>
                  </ul>
                </button>
              </div>
            </div>
          </li>
          
          <!-- Illustrator -->
          <li class="adobe-product">
            <div class="products">
              <svg viewBox="0 0 52 52" style="border:1px solid #b65a0b">
                <g xmlns="http://www.w3.org/2000/svg">
                  <path d="M40.824 52H11.176C5.003 52 0 46.997 0 40.824V11.176C0 5.003 5.003 0 11.176 0h29.649C46.997 0 52 5.003 52 11.176v29.649C52 46.997 46.997 52 40.824 52z" fill="#261400" data-original="#6d4c13" />
                  <path d="M30.68 39h-3.24l-2.76-9.04h-8.32L13.72 39H10.6l8.24-28h3.32l8.52 28zm-6.72-12l-3.48-11.36L17.12 27h6.84zM37.479 12.24c0 .453-.16.84-.48 1.16-.32.319-.7.479-1.14.479-.44 0-.827-.166-1.16-.5-.334-.333-.5-.713-.5-1.14s.166-.807.5-1.141c.333-.333.72-.5 1.16-.5.44 0 .82.16 1.14.48.321.322.48.709.48 1.162zM37.24 39h-2.88V18.96h2.88V39z" fill="#e6d2c0" data-original="#ffbd2e" />
                </g>
              </svg>
              Illustrator
            </div>
            
            <span class="status">
              <span class="status-circle"></span>
              可更新
            </span>
            <div class="button-wrapper">
              <button class="content-button status-button">更新此应用</button>
              <div class="pop-up">
                <div class="pop-up__title">更新此应用
                  <svg class="close" width="24" height="24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                    <circle cx="12" cy="12" r="10" />
                    <path d="M15 9l-6 6M9 9l6 6" />
                  </svg>
                </div>
                <div class="pop-up__subtitle">继续前请根据需要调整高级选项。<a href="#">了解更多</a></div>
                <div class="checkbox-wrapper">
                  <input type="checkbox" id="check1" class="checkbox">
                  <label for="check1">导入以前的设置和偏好</label>
                </div>
                <div class="checkbox-wrapper">
                  <input type="checkbox" id="check2" class="checkbox">
                  <label for="check2">移除旧版本</label>
                </div>
                <div class="content-button-wrapper">
                  <button class="content-button status-button open close">取消</button>
                  <button class="content-button status-button">更新</button>
                </div>
              </div>
            </div>
          </li>
        </ul>
      </div>
      
      <!-- 推荐应用部分 -->
      <div class="content-section">
        <div class="content-section-title">推荐应用</div>
        <div class="apps-card">
          <AppCard 
            title="Premiere Pro" 
            subtext="视频编辑软件"
            icon="https://assets.codepen.io/3364143/1.png"
          />
          <AppCard 
            title="After Effects" 
            subtext="视觉效果软件"
            icon="https://assets.codepen.io/3364143/2.png"
          />
          <AppCard 
            title="Dreamweaver" 
            subtext="网页设计软件"
            icon="https://assets.codepen.io/3364143/3.png"
          />
          <AppCard 
            title="XD" 
            subtext="UI/UX设计软件"
            icon="https://assets.codepen.io/3364143/4.png"
          />
          <AppCard 
            title="Premiere Rush" 
            subtext="视频编辑软件"
            icon="https://assets.codepen.io/3364143/5.png"
          />
          <AppCard 
            title="Fresco" 
            subtext="绘画软件"
            icon="https://assets.codepen.io/3364143/6.png"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.main-container {
  display: flex;
  flex-direction: column;
  flex-grow: 1;
  overflow: hidden;
}

.main-header {
  display: flex;
  align-items: center;
  border-bottom: 1px solid var(--border-color);
  height: 58px;
  flex-shrink: 0;
  padding: 0 30px;
}

.menu-link-main {
  text-decoration: none;
  color: var(--theme-color);
  display: none;
}

.main-header .header-menu {
  margin-left: 150px;
}

.main-header .header-menu a {
  padding: 20px 24px;
}

.content-wrapper {
  display: flex;
  flex-direction: column;
  color: var(--theme-color);
  padding: 20px 40px;
  height: 100%;
  overflow: auto;
  background-color: var(--theme-bg-color);
}

.content-wrapper-header {
  display: flex;
  align-items: center;
  width: 100%;
  justify-content: space-between;
  background-image: url("https://www.transparenttextures.com/patterns/cubes.png"), linear-gradient(to right top, #cf4af3, #e73bd7, #f631bc, #fd31a2, #ff3a8b, #ff4b78, #ff5e68, #ff705c, #ff8c51, #ffaa49, #ffc848, #ffe652);
  border-radius: 14px;
  padding: 20px 40px;
}

.content-wrapper-context {
  max-width: 350px;
}

.content-wrapper-context h3 {
  font-size: 24px;
  font-weight: 700;
  color: #fff;
  margin: 12px 0;
}

.content-text {
  line-height: 1.5em;
  color: #fff;
  font-size: 14px;
  margin: 12px 0;
}

.content-button {
  background-color: #fff;
  border: none;
  padding: 8px 26px;
  color: #ff3a8b;
  border-radius: 20px;
  margin-top: 16px;
  cursor: pointer;
  transition: 0.3s;
  white-space: nowrap;
}

.content-button:hover {
  background: rgba(255, 255, 255, 0.9);
}

.content-wrapper-img {
  width: 186px;
  object-fit: cover;
  margin-top: -25px;
  object-position: center;
}

.content-section {
  margin-top: 30px;
  display: flex;
  flex-direction: column;
}

.content-section-title {
  color: var(--content-title-color);
  margin-bottom: 14px;
}

.content-section ul {
  display: flex;
  flex-direction: column;
  width: 100%;
  height: 100%;
  background-color: var(--content-bg);
  padding: 20px;
  border-radius: 14px;
}

.content-section ul li {
  list-style: none;
  padding: 10px;
  margin: 12px 0;
  border-radius: 6px;
  background-color: var(--theme-bg-color);
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.content-section ul li:hover {
  background-color: var(--theme-bg-color);
}

.content-section ul li + li {
  margin-top: 10px;
}

.products {
  display: flex;
  align-items: center;
}

.products svg {
  width: 28px;
  border-radius: 6px;
  margin-right: 12px;
}

.status {
  margin-left: auto;
  display: flex;
  align-items: center;
}

.status-circle {
  width: 6px;
  height: 6px;
  background-color: #ccc;
  border-radius: 50%;
  margin-right: 8px;
}

.status-circle.green {
  background-color: #3bf083;
}

.status-button {
  font-size: 15px;
  margin-left: 10px;
  padding: 6px 24px;
}

.status-button.open {
  background: none;
  color: var(--button-inactive);
  border: 1px solid var(--button-inactive);
}

.status-button:not(.open):hover {
  color: #fff;
  background: var(--button-inactive);
}

.content-button:not(.open):hover {
  background: #1e59f1;
}

.menu {
  width: 5px;
  height: 5px;
  background-color: var(--button-inactive);
  border-radius: 50%;
  box-shadow: 7px 0 0 0 var(--button-inactive), 14px 0 0 0 var(--button-inactive);
  margin: 0 12px;
}

.dropdown {
  position: relative;
  height: 53px;
  width: 40px;
  top: -20px;
  display: flex;
  left: -16px;
  background: transparent;
  border: none;
  cursor: pointer;
}

.dropdown ul {
  position: absolute;
  background: var(--dropdown-bg);
  height: 110px;
  width: 120px;
  right: 0;
  top: 20px;
  pointer-events: none;
  opacity: 0;
  transform: translatey(10px);
  transition: all 0.3s ease;
}

.dropdown.is-active ul {
  pointer-events: all;
  opacity: 1;
  transform: translatey(25px);
}

.dropdown.is-active ul li:hover {
  background-color: var(--dropdown-hover);
}

.button-wrapper {
  display: flex;
  align-items: center;
  justify-content: flex-end;
}

.pop-up {
  position: absolute;
  padding: 30px 40px;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  overflow-y: auto;
  box-shadow: 0px 6px 30px rgba(0, 0, 0, 0.4);
  transition: all 0.3s;
  z-index: 10;
  background-color: var(--popup-bg);
  width: 500px;
  visibility: hidden;
  opacity: 0;
  border-radius: 6px;
}

.pop-up.visible {
  visibility: visible;
  opacity: 1;
}

.pop-up__title {
  padding-bottom: 20px;
  border-bottom: 1px solid var(--border-color);
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.pop-up__subtitle {
  white-space: normal;
  margin: 20px 0;
}

.pop-up__subtitle a {
  color: var(--theme-color);
}

.checkbox-wrapper {
  margin: 8px 0;
}

.checkbox-wrapper + .checkbox-wrapper {
  margin: 20px 0;
}

.checkbox {
  display: none;
}

.checkbox + label {
  display: flex;
  align-items: center;
}

.checkbox + label:before {
  content: "";
  margin-right: 10px;
  width: 15px;
  height: 15px;
  border: 1px solid var(--theme-color);
  border-radius: 4px;
  cursor: pointer;
  flex-shrink: 0;
}

.checkbox:checked + label:before {
  background-color: #3a6df0;
  border-color: #3a6df0;
  background-image: url("data:image/svg+xml;charset=UTF-8,%3csvg xmlns='http://www.w3.org/2000/svg' width='24' height='24' viewBox='0 0 24 24' fill='none' stroke='%23fff' stroke-width='3' stroke-linecap='round' stroke-linejoin='round' class='feather feather-check'%3e%3cpath d='M20 6L9 17l-5-5'/%3e%3c/svg%3e");
  background-position: 50%;
  background-size: 12px;
  background-repeat: no-repeat;
}

.content-button-wrapper {
  margin-top: 20px;
  display: flex;
  align-items: center;
  justify-content: flex-end;
}

.content-button-wrapper .open {
  margin-right: 8px;
}

.apps-card {
  display: flex;
  flex-wrap: wrap;
  width: calc(100% + 20px);
  margin-left: -10px;
}

.close {
  position: absolute;
  right: 0;
  top: 0;
  z-index: 2;
  cursor: pointer;
  width: 24px;
  height: 24px;
}

.overlay-app {
  width: 100%;
  height: 100%;
  position: fixed;
  left: 0;
  top: 0;
  pointer-events: all;
  background-color: rgba(36, 39, 59, 0.8);
  opacity: 0;
  visibility: hidden;
  transition: 0.3s;
}

.overlay-app.is-active {
  visibility: visible;
  opacity: 1;
}

@media screen and (max-width: 1110px) {
  .main-header .header-menu {
    margin-left: 20px;
  }
  
  .menu-link-main {
    display: block;
  }
}

@media screen and (max-width: 768px) {
  .main-header .header-menu a:not(.is-active) {
    display: none;
  }
  
  .content-wrapper-img {
    width: 110px;
  }
}

@media screen and (max-width: 480px) {
  .content-wrapper {
    padding: 10px 20px 20px;
  }
  
  .content-wrapper-header {
    padding: 20px;
  }
  
  .menu-link-main {
    margin-left: 0;
  }
}
</style> 