<template>
        <!-- <p>{{counter}}</p> -->
        <p>We do more...</p>
</template>

<script>
export default {
  computed: {
    counter() {
    //   return this.$store.state.counter;
        return this.$store.getters.finalCounter;
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