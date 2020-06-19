<template>
  <div id="app"> 
    <Header/>
    <List/>
  </div>
</template>

<script>
import Header from './components/Header'
//import HelloWorld from './components/HelloWorld.vue'
import List from './components/List'
//import Detail from './components/Detail'

export default {
  name: 'App',
  components: {
    List,
    Header
    //Detail
  }
}
</script>