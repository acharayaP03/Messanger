<script setup>
import { Header, ConversationArea } from  './components'
import {UserDetails, UserDetailsHeader } from  './components/UserDetails'
import ChatArea from "./components/ChatArea.vue";

</script>

<template>
  <Header/>
    <main class="wrapper">
      <ConversationArea/>
      <ChatArea/>
      <div class="detail-area">
        <UserDetailsHeader/>
        <UserDetails/>
    </div>
    </main>

</template>
