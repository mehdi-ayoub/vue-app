<template>
  <nav>
    <div class="container-nav">
      <h1> My Vue App </h1>
    </div>
  </nav>

  <div class="components">
    <HeaderApp class="first-component"/>
    <ConditionalComp/>
  </div>
</template>

<script>
import HeaderApp from './components/HeaderApp.vue'
import ConditionalComp from './components/ConditionalComp.vue';

export default {
  name: 'App',
  components: {
    HeaderApp, ConditionalComp
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

}

.container-nav {
    background-color: grey;
    color: white;
    height: 70px;
    display: flex;
    align-items: center;
  }

  .container-nav h1 {
    font-size: 200;
    margin-left: 5px;
    color: aqua;
  }

html, body {
  margin: 0;
  padding: 0
}

.components {
  display: flex;
  flex-direction: row;
  align-items: center;
  margin-right: 50px;
}

</style>
