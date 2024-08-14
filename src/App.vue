<script setup>
import HeaderBoard from './components/HeadBoard.vue'
import SideBoard from './components/SideBoard.vue'
import MainBoard from './components/MainBoard.vue'
import WidgetOne from './components/WidgetOne.vue'
import widgetTwo from './components/WidgetTwo.vue'
import widgetThree from './components/WidgetThree.vue'
import widgetFour from './components/WidgetFour.vue'
// import widgetFive from './components/WidgetFive.vue'
</script>

<template>
  <div name="app">
    <HeaderBoard />
    <SideBoard />
    <MainBoard />
    <WidgetOne />
    <widgetTwo />
    <widgetThree />
    <widgetFour />
    <!-- <widgetFive /> -->
    <nav>
      <!-- <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/about">About</RouterLink> -->
    </nav>
    <!-- <RouterView /> -->
  </div>
</template>

<style>
body {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
</style>
