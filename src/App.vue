<template>
<DataNews />

<DemoData />

<DemoDataTwo />

<CheckMethod />

<CheckInputData />
</template>

<script>

import DataNews from './components/DataNews.vue'
import DemoData from './components/DemoData.vue'
import DemoDataTwo from './components/DemoDataTwo.vue'
import CheckMethod from './components/CheckMethod.vue'
import CheckInputData from './components/CheckInputData.vue'


export default {
  name: 'App',
  components: {
          DataNews,
          DemoData,
          DemoDataTwo,
          CheckMethod,
          CheckInputData
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
