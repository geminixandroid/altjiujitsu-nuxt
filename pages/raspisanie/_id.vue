<template>
  <v-main>
    {{$route.params.id}}
    {{ip}}
  </v-main>
</template>

<script>
  export default {
    /*async asyncData({ $axios }) {
      const ip = await $axios.$get('http://icanhazip.com')
      return { ip }
    },*/
    asyncData({ $axios }) {
      return $axios.$get('http://icanhazip.com').then(res=>{
        console.log(res)
        return {ip:res}}
        )
    }
  }
</script>

<style scoped>

</style>
