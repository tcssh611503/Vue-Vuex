<template>
        <h3>{{counter}}</h3>
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
        this.$store.state.counter = this.$store.state.counter +11;
    }
  },
    
}
</script>