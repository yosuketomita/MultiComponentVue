<script setup lang="ts">
import Child2 from './components/Child2.vue'
import Child1 from './components/Child1.vue'
import { ref } from 'vue'

const elements = ref([])
const msg = ref(['hello'])
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <Child2 :msg="'You did it!'" />
      
    </div>
  </header>

  <main>
    <Child1  v-model="elements"></Child1>

    
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
