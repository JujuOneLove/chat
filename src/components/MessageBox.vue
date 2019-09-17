<template>
  <div>
    <form @submit.prevent="onFormSubmit">
      <input type="text" placeholder="Tape ton message ..." v-model="message"/>
    </form>
  </div>
</template>

<script>
export default {
  name: 'MessageBox',
  data () {
    return {
      message: ''
    }
  },
  methods: {
    onFormSubmit () {
      this.$emit('messageSent', this.message)
      this.message = ''
    }
  }
}
</script>
