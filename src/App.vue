<script setup>
import TableView from './components/TableView.vue';
import PanelView from './components/PanelView.vue'
</script>

<template>
  <header>
    <h1 class="title">
      Тестовое задание СТЕК
    </h1>
  </header>

  <main>
    <div :style="{padding: '0 50px'}">
      <PanelView />
      <TableView />
    </div>
  </main>
</template>

<style scoped>
.title {
  text-align: center;
}
</style>
