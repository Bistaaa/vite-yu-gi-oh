<script>
import { store } from './store.js';
import AppHeader from './components/AppHeader.vue'
import CardList from './components/cardList.vue'

export default {
  components: {
    AppHeader,
    CardList
  },
  data() {
    return {
      store
    }
  },
  methods: {
    getCards() {
      axios.get(store.apiURL)
    }
  }

}
</script>

<template>
  <div>
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  <HelloWorld msg="Vite + Vue" />
</template>

<style scoped></style>
