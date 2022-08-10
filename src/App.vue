<template>
  <div>
    <center>
      <hr><br><br>
        <img alt="Vue logo" class="logoSvg" src="./assets/logo.svg" />
      <br><br><hr><br><br>
      <button @click="component='reactivity-component'">Reactivity</button>
      <button @click="component='conditional-rendering'">Conditional</button>
      <button @click="component='list-rendering'">List Rendering</button>

      <br><br><br><hr><br><br>
      <keep-alive><component v-bind:is="component"/></keep-alive>
    </center>
  </div>
</template>

<script>
import ReactivityComponent from './components/ReactivityComponent.vue';
import ConditionalRendering from './components/ConditionalRendering.vue';
import ListRendering from './components/ListRendering.vue';

export default{
  name: 'App',
  components:{
    'reactivity-component': ReactivityComponent,
    'conditional-rendering': ConditionalRendering,
    'list-rendering': ListRendering,
  },
    data(){
      return{
          component: 'list-rendering'
      }
    }
}

</script>

<style scoped>
  .logoSvg{
    width: 10%;
  }
</style>