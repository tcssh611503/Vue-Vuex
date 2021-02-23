<template>
  <base-container title="Vuex">
    <!-- <h3>{{counter}}</h3>-->  
    <button @click="addOne" >Add 2</button> 
    <the-counter></the-counter>
    <favorite-value></favorite-value>
    <change-counter></change-counter>
  </base-container>
</template>

<script>
import BaseContainer from './components/BaseContainer.vue';
import TheCounter from './components/TheCounter.vue';
import ChangeCounter from './components/ChangeCounter.vue';
import FavoriteValue from './components/FavoriteValue.vue';


export default {
  components: {
    BaseContainer,
    TheCounter,
    ChangeCounter,
    FavoriteValue
  },
  // computed: {
  //   counter() {
  //     return this.$store.state.counter;
  //   }
  // },
  methods: {
    addOne(){
      // this.$store.state.counter++;
      // this.$store.state.counter = this.$store.state.counter +11;
      // this.$store.commit('increase', {value: 2});

      // this.$store.commit({
      //   type: 'increase',
      //   value: 10
      // });

      this.$store.dispatch({
        type: 'increase',
        value: 10
      });

    }
  },

  data(){


  }



};
</script>

<style>
* {
  box-sizing: border-box;
}

html {
  font-family: sans-serif;
}

body {
  margin: 0;
}
</style>