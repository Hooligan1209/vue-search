<template>
  <div class="container">
    <search @getName="getName"></search>
    <user :username="username"></user>
  </div>
</template>

<script>
import user from './components/users.vue'
import search from './components/search.vue'
export default {
    data () {
       return {
           username :''
       }
    },
    components: {
      user,
      search
    },
  methods: {
    getName (username) {
        this.username = username
    }
  }
}
</script>

<style>

</style>
