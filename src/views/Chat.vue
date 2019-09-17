<template>
  <div class="chat">
    <UsersList/>
    <MessagesList :messages=messages />
    <MessageBox @messageSent="onMessageSent"/>
  </div>
</template>

<script>
// @ is an alias to /src
import UsersList from '../components/UsersList.vue'
import MessagesList from '../components/MessagesList.vue'
import MessageBox from '../components/MessageBox.vue'

export default {
  name: 'chat',
  data: function () {
    return {
      messages: []
    }
  },
  components: {
    UsersList,
    MessagesList,
    MessageBox
  },
  methods: {
    onMessageSent (message) {
      this.messages.push(message)
    }
  }
}
</script>
