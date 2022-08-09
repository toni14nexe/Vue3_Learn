<template>
  <div>
    <hr><br><br>
      <img alt="Vue logo" class="logoSvg" src="./assets/logo.svg" />
    <br><br><hr><br><br>
    <center>
      <button @click="component='reactivity-component'">Async</button>


      <br><br><br><hr><br><br>
      <keep-alive><component v-bind:is="component"/></keep-alive>
    </center>
  </div>
</template>

<script>
import ReactivityComponent from './components/ReactivityComponent.vue';

export default{
  name: 'App',
  components:{
    'reactivity-component': ReactivityComponent
  },
    data(){
      return{
          component: 'reactivity-component'
      }
    }
}

</script>

<style scoped>
  .logoSvg{
    width: 50%;
    margin-left: 25%;
  }
</style>