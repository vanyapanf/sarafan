<template>
  <div>
    <div v-if="!profile">Необходимо авторизоваться через
      <a href="/login">Google</a>
    </div>
    <div v-else>
      <div>{{profile.name}}&nbsp;<a href="/logout">Выйти</a></div>
      <message-list :messages = "messages" />
    </div>
  </div>
</template>

<script>
  import MessageList from 'components/messages/MessageList.vue'

  export default {
    components: {
      MessageList
    },
    data() {
      return {
        messages: frontendData.messages,
        profile: frontendData.profile
      }
    }
  }
</script>

<style>

</style>