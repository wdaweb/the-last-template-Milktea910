<template>
  <q-layout view="hHh Lpr fff">
    <!-- 可選的 Header：你也可以改成引入 TheHeader.vue -->
    <q-header elevated class="header text-white">
      <q-toolbar class="q-px-lg">
        <q-toolbar-title>
          <img
            src="https://preview.treethemes.com/hazel/demo2/wp-content/uploads/sites/12/2021/04/logo_light.png"
            alt="Logo"
            height="18"
          />
        </q-toolbar-title>
        <div v-if="!isMobile">
          <q-tabs v-model="tab" shrink>
            <q-tab name="HOME" label="HOME" @click="scrollToSection('Hero')" />
            <q-tab name="ABOUT" label="ABOUT" @click="scrollToSection('About')" />
            <q-tab name="SERVICES" label="SERVICES" @click="scrollToSection('Choose')" />
            <q-tab name="WORK" label="WORK" @click="scrollToSection('Work')" />
            <q-tab name="CLIENT" label="CLIENT" @click="scrollToSection('Client')" />
            <q-tab name="CONTACTS" label="CONTACTS" @click="scrollToSection('Contacts')" />
          </q-tabs>
        </div>
        <div v-else>
          <q-btn-dropdown dropdown-icon="menu" no-caps flat>
            <q-list>
              <q-item clickable v-close-popup tabindex="0" @click="scrollToSection('Hero')">
                <q-item-section>
                  <q-item-label>HOME</q-item-label>
                </q-item-section>
              </q-item>
              <q-item clickable v-close-popup tabindex="0" @click="scrollToSection('About')">
                <q-item-section>
                  <q-item-label>ABOUT</q-item-label>
                </q-item-section>
              </q-item>
              <q-item clickable v-close-popup tabindex="0" @click="scrollToSection('Choose')">
                <q-item-section>
                  <q-item-label>SERVICES</q-item-label>
                </q-item-section></q-item
              >
              <q-item clickable v-close-popup tabindex="0" @click="scrollToSection('Work')">
                <q-item-section>
                  <q-item-label>WORK</q-item-label>
                </q-item-section></q-item
              >
              <q-item clickable v-close-popup tabindex="0" @click="scrollToSection('Client')">
                <q-item-section>
                  <q-item-label>CLIENT</q-item-label>
                </q-item-section></q-item
              >
              <q-item clickable v-close-popup tabindex="0" @click="scrollToSection('Contacts')">
                <q-item-section>
                  <q-item-label>CONTACTS</q-item-label>
                </q-item-section></q-item
              >
            </q-list>
          </q-btn-dropdown>
        </div>

        <div v-if="!isMobile">
          <q-btn flat to="/contacts"><q-icon size="large" name="facebook"></q-icon></q-btn>
          <q-btn flat to="/contacts"
            ><q-icon size="large" name="fa-brands fa-twitter"></q-icon
          ></q-btn>
          <q-btn flat to="/contacts"
            ><q-icon size="large" name="fa-brands fa-instagram"></q-icon
          ></q-btn>
          <q-btn flat to="/contacts"
            ><q-icon size="large" name="fa-brands fa-tiktok"></q-icon
          ></q-btn>
        </div>
      </q-toolbar>
    </q-header>

    <!-- 主內容區 -->
    <q-page-container>
      <router-view />
    </q-page-container>

    <!-- 頁尾 -->
    <q-footer class="footer text-white text-center q-pa-md">
      <div class="image">
        <img
          src="https://preview.treethemes.com/hazel/demo2/wp-content/uploads/sites/12/2021/04/logo_light.png"
          alt="Logo"
          height="18"
        />
      </div>
      <div class="icon">
        <q-btn flat to="/contacts"><q-icon size="large" name="facebook"></q-icon></q-btn>
        <q-btn flat to="/contacts"
          ><q-icon size="large" name="fa-brands fa-twitter"></q-icon
        ></q-btn>
        <q-btn flat to="/contacts"
          ><q-icon size="large" name="fa-brands fa-instagram"></q-icon
        ></q-btn>
        <q-btn flat to="/contacts"><q-icon size="large" name="fa-brands fa-tiktok"></q-icon></q-btn>
      </div>
      &copy; 2025 泰山職訓中心 作業練習
    </q-footer>
  </q-layout>
</template>

<script setup>
import { ref, computed, onMounted, onUnmounted } from 'vue'

const tab = ref('HOME')
const width = ref(window.innerWidth)
const BREAKPOINT = 800

const isMobile = computed(() => width.value < BREAKPOINT)

function scrollToSection(id) {
  const el = document.getElementById(id)
  if (el) {
    el.scrollIntoView({ behavior: 'smooth' })
  }
}

function handleResize() {
  width.value = window.innerWidth
}
onMounted(() => {
  window.addEventListener('resize', handleResize)
})
onUnmounted(() => {
  window.removeEventListener('resize', handleResize)
})
</script>
<style scoped>
.image {
  margin-bottom: 2rem;
}
.icon {
  margin-bottom: 2rem;
}
.header {
  background: rgb(16, 16, 16);
}
.footer {
  background: rgb(16, 16, 16);
  height: 200px;
}
</style>
