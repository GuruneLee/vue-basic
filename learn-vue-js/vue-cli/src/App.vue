<template>
  <div>
    <!-- <app-header v-bind:프롭스속성이름="상위컴포넌트의데이터이름"></app-header> -->
    <app-header 
      v-bind:propsdata="str"
      v-on:renew="renewStr"></app-header>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
export default {
  data: function(){
    return {
      str: 'Header'
    }
  },
  components: {
    'app-header': AppHeader
  },
  methods: {
    renewStr() {
      this.str = 'renew';
    }
  }
}
</script>

<style>

</style>