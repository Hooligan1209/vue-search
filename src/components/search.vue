<template>
  <section class="jumbotron">
    <h3 class="jumbotron-heading">Search Github Users</h3>
    <div>
      <input type="text" placeholder="enter the name you search" v-model="searchName"  @keyup.enter="search"/>
      <button @click="search">Search</button>
    </div>
  </section>
</template>

<script>
  export default {
      data () {
          return {
              searchName: ''
          }
      },
    methods: {
      search () {
          this.$emit('getName' , this.searchName)
      }
    }
  }
</script>

<style>

</style>
