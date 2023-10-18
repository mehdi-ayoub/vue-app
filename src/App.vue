<template>
  <nav>
    <div class="container-nav">
      <h1> My Vue App </h1>
    </div>
  </nav>

  <div class="components">
    <HeaderApp class="first-component"/>
    <ConditionalComp/>
    <conditionalComp2/>
    <TextareaCounting/>
    <ChangeInput/>
    <ClickModelConditional/>
  </div>
</template>

<script>
import HeaderApp from './components/HeaderApp.vue'
import ConditionalComp from './components/ConditionalComp.vue';
import ConditionalComp2 from './components/ConditionalComp2.vue'
import TextareaCounting from './components/TextareaCounting.vue'
import ChangeInput from './components/ChangeInput.vue'
import ClickModelConditional from './components/ClickModelConditional.vue'

export default {
  name: 'App',
  components: {
    HeaderApp, ConditionalComp, ConditionalComp2, TextareaCounting, ChangeInput, ClickModelConditional
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
  flex-wrap: wrap;
}

</style>
