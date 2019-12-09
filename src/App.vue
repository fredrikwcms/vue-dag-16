<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <!-- <HelloWorld msg="ASdf"/> -->
    <!-- <MyTitle title="Here's my main title"/>
    <MyArticle class="container" articleTitle="Here's my article title"/> -->
    <!-- <MyTodoList/> -->
    <tabs>
      <tab name="My first tab" :selected="true">
        <h1>My first tab</h1>
      </tab>
      <tab name="My second tab">
        <h1>My second tab</h1>
      </tab>
      <tab name="My third tab">
        <h1>My third tab</h1>
        <MyTodoList/>
      </tab>
    </tabs>
    <Accordion/>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
// import MyTitle from './components/MyTitle.vue'
// import MyArticle from './components/MyArticle.vue'
import MyTodoList from './components/MyTodoList.vue'
import Tab from './components/Tab.vue'
import Tabs from './components/Tabs.vue'
import Accordion from './components/Accordion.vue'

import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

export default {
  name: 'app',
  components: {
    // HelloWorld
    // MyTitle,
    // MyArticle,
    MyTodoList,
    Tabs,
    Tab,
    Accordion
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
