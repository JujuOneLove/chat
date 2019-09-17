<template>
  <ul>
    <li v-for="(message, index) in messages" :key="index">{{message}}</li>
  </ul>
</template>

<script>
export default {
  name: 'MessagesList',
  props: ['messages']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
