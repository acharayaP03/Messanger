
<script setup>
import {reactive, ref} from 'vue'
const status = ref(false)
const active = ref(false)
const users = reactive([
  {
    user: 'Madison Jones',
    userProfileImage: 'https://s3-us-west-2.amazonaws.com/s.cdpn.io/3364143/download+%281%29.png',
    status: true,
    recentMessage: 'What time was our meet',
    lastUpdate: '20m'
  },
  {
    user: 'Miguel Cohen',
    userProfileImage: 'https://s3-us-west-2.amazonaws.com/s.cdpn.io/3364143/download+%2812%29.png',
    status: true,
    recentMessage: 'Adaptogen taiyaki austin jean shorts brunch',
    lastUpdate: '20m'
  },
  {
    user: 'Lea Debere',
    userProfileImage: 'https://s3-us-west-2.amazonaws.com/s.cdpn.io/3364143/download+%282%29.png',
    status: true,
    recentMessage: 'Shoreditch iPhone jianbing',
    lastUpdate: '45m'
  },
  {
    user: 'Jordan Smith',
    userProfileImage: 'https://s3-us-west-2.amazonaws.com/s.cdpn.io/3364143/download+%281%29+%281%29.png',
    status: true,
    recentMessage: 'Snackwave craft beer raclette, beard kombucha',
    lastUpdate: '2hr'
  },
  {
    user: 'Jared Jackson',
    userProfileImage: 'https://s3-us-west-2.amazonaws.com/s.cdpn.io/3364143/download+%284%29+%281%29.png',
    status: true,
    recentMessage: 'Tattooed brooklyn typewriter gastropub',
    lastUpdate: '2hr 2 mins'
  },
  {
    user: 'Henry Clark',
    userProfileImage: 'https://s3-us-west-2.amazonaws.com/s.cdpn.io/3364143/download+%283%29+%281%29.png',
    status: true,
    recentMessage: 'Ethical typewriter williamsburg lo-fi street art',
    lastUpdate: '2hr'
  },
  {
    user: 'Jason Mraz',
    userProfileImage: 'https://s3-us-west-2.amazonaws.com/s.cdpn.io/3364143/qs6F3dgm.png',
    status: true,
    recentMessage: 'I\'m lucky I\'m in love with my best friend',
    lastUpdate: '5hr'
  },
  {
    user: 'Chiwa Lauren',
    userProfileImage: 'https://s3-us-west-2.amazonaws.com/s.cdpn.io/3364143/download+%288%29.png',
    status: true,
    recentMessage: 'Pabst af 3 wolf moon',
    lastUpdate: '5hr'
  },
  {
    user: 'Caroline Orange',
    userProfileImage: 'https://s3-us-west-2.amazonaws.com/s.cdpn.io/3364143/download+%289%29.png',
    status: true,
    recentMessage: 'Bespoke aesthetic lyft woke cornhole',
    lastUpdate: '35m'
  },
  {
    user: 'Lina Ashma',
    userProfileImage: 'https://s3-us-west-2.amazonaws.com/s.cdpn.io/3364143/download+%286%29.png',
    status: true,
    recentMessage: 'Migas food truck crucifix vexi',
    lastUpdate: '42m'
  }
])
</script>
<template>
  <v-list>
    <v-list-item
        class="msg"
        v-for="(user, userIndex) in users"
        :key="userIndex"
        :prepend-avatar="user.userProfileImage"
    >
      <v-badge dot color="success" />
      <v-list-item-title class="msg-detail">
        <div class="msg-username">{{ user.user}}</div>
      </v-list-item-title>
      <v-list-item-subtitle class="msg-content">
        <span class="text-grey-darken-4 text-truncate">{{ user.recentMessage}}</span>
      </v-list-item-subtitle>
      <v-list-item-action class="mt-1"> <span class="msg-date ml-auto">{{ user.lastUpdate}}</span></v-list-item-action>
    </v-list-item>
  </v-list>
</template>

<style scoped lang="scss">

  .msg-profile {
    width: 44px;
    height: 44px;
    border-radius: 50%;
    object-fit: cover;
    margin-right: 15px;

    &.group {
      display: flex;
      justify-content: center;
      align-items: center;
      background-color: var(--border-color);

      svg {
        width: 60%;
      }
    }
  }

  :deep(.v-list-item__content){
    flex: 1;
  }
  .msg {
    display: flex;
    align-items: center;
    cursor: pointer;
    transition: 0.2s;
    position: relative;

    &:hover {
     background-color: var(--msg-hover-bg);
    }
    &.active {
       background: var(--active-conversation-bg);
       border-left: 4px solid var(--theme-color);
    }
    &.online:before {
       content: "";
       position: absolute;
       background-color: #23be7e;
       width: 9px;
       height: 9px;
       border-radius: 50%;
       border: 2px solid var(--theme-bg-color);
       left: 50px;
       bottom: 19px;
     }
    }

    .msg-username {
      margin-bottom: 4px;
      font-weight: 600;
      font-size: 15px;
    }

    .msg-detail {
      overflow: hidden;
    }

    .msg-content {
      font-weight: 500;
      font-size: 13px;
      display: flex;
    }

    .msg-message {
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
      color: var(--msg-message);
    }

    .msg-date {
      font-size: 14px;
      color: var(--msg-date);
      margin-left: 3px;
      &:before {
         content: "•";
         margin-right: 2px;
     }
    }
</style>