<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import ChristmasTree from './components/ChristmasTree.vue'
import Pivot from './components/Pivot.vue'
import '@webdatarocks/webdatarocks/theme/teal/webdatarocks.css'
</script>

<template>
  <header>
    <link rel="stylesheet" type="text/css" href="theme/teal/webdatarocks.min.css" />

    <div class="wrapper">
      <div class="pivot-container">
        <div class="logo">📊 Vue 3 + WebDataRocks</div>
        <Pivot toolbar />
      </div>
      <ChristmasTree />
    </div>
  </header>
</template>

<style scoped>
.pivot-container {
  width: 100%;
}
:root {
  --color-primary: #00796b;
  --color-secondary: #004d40;
  --color-text: #ffffff;
  --color-background: #e0f2f1;
  --color-border: #004d40;
}

header {
  background: var(--color-primary);
  color: var(--color-text);
  padding: 1rem;
  border-bottom: 3px solid var(--color-secondary);
}

.logo {
  font-size: 1.5rem;
  text-align: center;
  font-weight: bold;
  margin-bottom: 1rem;
}

nav a {
  color: var(--color-text);
  text-decoration: none;
  padding: 0.5rem 1rem;
  transition: all 0.3s ease;
}

nav a:hover {
  background: var(--color-secondary);
  border-radius: 4px;
}

nav a.router-link-exact-active {
  font-weight: bold;
  text-decoration: underline;
}

.wrapper {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  gap: 10rem;
}
@media (min-width: 1024px) {
  header {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .wrapper {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
  }

  nav {
    margin-top: 0;
  }
}
.pivot-container {
  display: flex;
  flex-direction: column;
}
</style>
