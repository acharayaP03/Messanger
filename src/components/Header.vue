<template>
  <header class="header">
    <div class="logo d-flex justify-center align-center">
      <v-icon icon="mdi-facebook-messenger" color="white" size="40"></v-icon>
    </div>
    <div class="search-bar">
      <v-text-field variant="plain" placeholder="search" append-icon/>
    </div>
    <div class="user-settings">
      <div class="dark-light">
        <v-icon icon="mdi-weather-night"></v-icon>
      </div>
      <div class="settings">
        <v-icon icon="mdi-cog"></v-icon>
      </div>
      <v-avatar>
        <img class="user-profile" src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/3364143/download+%281%29.png" alt="">
      </v-avatar>
    </div>
  </header>
</template>


<style scoped lang="scss">

.search-bar {
  width: 100%;
  height: 80px;
  z-index: 3;
  position: relative;
  margin-left: 280px;

  :deep(.v-text-field) {
    .v-input__control{
      .v-field {
        &__field {
          & input{
            border-radius: 100px;
            height: 100%;
            width: 100%;
            display: block;
            border: none;
            color: var(--body-color);
            padding: 0 54px;
            font-family: var(--body-font);
            font-weight: 600;
            font-size: 15px;
            &::placeholder {
              color: var(--input-chat-color);
            }

            &::placeholder {
              color: var(--input-chat-color);
            }
          }
        }
      }
    }
  }

}

.logo {
  background: var(--theme-color);
  width: 60px;
  height: 60px;
  border-radius: 100%;

  flex-shrink: 0;
}

.user-settings {
  display: flex;
  align-items: center;
  cursor: pointer;
  margin-left: auto;
  flex-shrink: 0;
  & > * + * {
    margin-left: 14px;
  }
}

.dark-light {
  width: 22px;
  height: 22px;
  color: var(--settings-icon-color);
  flex-shrink: 0;

  svg {
    width: 100%;
    fill: transparent;
    transition: 0.5s;
  }
}

.user-profile {
  width: 40px;
  height: 40px;
  border-radius: 50%;
}

.settings {
  color: var(--settings-icon-color);
  width: 22px;
  height: 22px;
  flex-shrink: 0;
}
</style>