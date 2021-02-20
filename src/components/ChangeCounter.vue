<template>
  <button @click="addOne" >Add 10</button>
</template>

<script>
export default {
  computed: {
    counter() {
      return this.$store.state.counter;
    }
  },
  methods: {
    addOne(){
      // this.$store.state.counter++;
        // this.$store.state.counter = this.$store.state.counter +11;
      this.$store.commit('increase', {value: 10});
    }
  },
    
}
</script>