<template>
  <div class="about">
    <h1>カウント</h1>
  <p>{{ count }}</p>
  <p>
    <button @click="a">+</button>
    <button @click="b">-</button>
  </p>
  </div>
</template>

<script>
export default {
  data(){
    return {
      
    }
  },
  methods:{
    a(){
      this.$store.commit('increment')
    },
    b(){
      this.$store.commit('decrement')
    }
  },
  computed:{
    count(){
      return this.$store.getters.count
    }
  }
}
</script>