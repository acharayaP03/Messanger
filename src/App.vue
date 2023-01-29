<script setup>
import { Header, ConversationArea } from  './components'
import {UserDetails, UserDetailsHeader } from  './components/UserDetails'
import ChatArea from "./components/ChatArea/index.vue";

</script>

<template>
  <v-app>
    <Header/>
    <v-main class="wrapper">
        <ConversationArea/>
        <ChatArea/>
        <div class="detail-area">
          <UserDetailsHeader/>
          <UserDetails/>
        </div>
    </v-main>
  </v-app>
</template>

<style scoped lang="scss">

.v-application{
  max-height: 100vh;
  position: relative;
  overflow: auto;
}
</style>
