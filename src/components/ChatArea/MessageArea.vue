<template>
  <div class="chat-area-footer">
    <v-icon icon="mdi-video-outline" size="28" class="mr-2 text-grey-lighten-1"></v-icon>
    <v-icon icon="mdi-message-image-outline" size="20" class="mr-2 text-grey-lighten-1"></v-icon>
    <v-icon icon="mdi-plus-circle-outline" size="20" class="mr-2 text-grey-lighten-1"></v-icon>
    <v-icon icon="mdi-attachment" size="26" class="mr-2 text-grey-lighten-1"></v-icon>
    <v-icon icon="mdi-emoticon-outline" size="20" class="mr-2 text-grey-lighten-1"></v-icon>

    <v-text-field
        label=""
        placeholder="Type here ..."
        type="input"
        clearable
        class="chat-area-input"
        variant="plain"
    ></v-text-field>
  </div>
</template>

<style scoped lang="scss">
  .chat-area-footer {
    display: flex;
    border-top: 1px solid var(--border-color);
    width: 100%;
    padding: 10px 20px;
    align-items: center;
    background-color: var(--theme-bg-color);
    position: sticky;
    bottom: 0;
    left: 0;

    & svg {
      color: var(--settings-icon-color);
      width: 20px;
      flex-shrink: 0;
      cursor: pointer;

      &:hover {
        color: var(--settings-icon-hover);
      }

      & + svg {
        margin-left: 12px;
      }
    }

    .chat-area-input .v-input{
      border-radius: 100px;
    }

    :deep(.v-text-field) {
      .v-input__control{
        .v-field {
          &__field {
            & input{
              border-radius: 100px;
              background-color: var(--input-bg);
              color: var(--body-color);
              background-color: var(--input-bg);
              font-size: 15px;
              width: inherit;
              padding: 15px;
              margin-top: 10px;

              &::placeholder {
                color: var(--input-chat-color);
              }
            }
          }
        }
      }
    }
  }


</style>