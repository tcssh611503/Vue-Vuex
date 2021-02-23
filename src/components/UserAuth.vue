<template>
<dev>
 <h2>sss</h2>
 <button @click="login"  v-if="!isAuth" >Login</button>
 <button @click="logout"  v-if="isAuth" >Logout</button>
 </dev>
</template>

<script>
// import { mapGetters } from 'vuex';
export default {
   methods: {
   login(){
     this.$store.dispatch('login');
   },
   logout(){
     this.$store.dispatch('logout');
   }
 },
  computed: {
   isAuth(){
     return this.$store.getters.userIsAuthenticated;
   }
  },
};
</script>