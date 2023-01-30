<script setup>
import ConversationListItem from './ConversationListItem.vue'
</script>

<template>
  <div class="conversation-area">
    <ConversationListItem/>
    <button class="add"></button>
  </div>
</template>
<style scoped lang="scss">

.conversation-area {
  border-right: 1px solid var(--border-color);
  overflow-y: auto;
  overflow-x: hidden;
  display: flex;
  flex-direction: column;
  position: relative;
}

.add {
  position: absolute;
  bottom: 60px;
  right: 20px;
  background-color: var(--theme-color);
  width: 60px;
  height: 60px;
  border: 0;
  border-radius: 50%;
  background-image: url("data:image/svg+xml;charset=UTF-8,%3csvg xmlns='http://www.w3.org/2000/svg' width='24' height='24' fill='none' stroke='white' stroke-width='2' stroke-linecap='round' stroke-linejoin='round' class='feather feather-plus'%3e%3cpath d='M12 5v14M5 12h14'/%3e%3c/svg%3e");
  background-repeat: no-repeat;
  background-position: 50%;
  background-size: 28px;
  box-shadow: 0 0 16px var(--theme-color);
  margin: auto auto -55px;
  flex-shrink: 0;
  z-index: 1;
  cursor: pointer;
}

.chat-area {
  display: flex;
  flex-direction: column;
  overflow: auto;
  &-header {
    display: flex;
    position: sticky;
    top: 0;
    left: 0;
    z-index: 2;
    width: 100%;
    align-items: center;
    justify-content: space-between;
    padding: 20px;
    background: var(--chat-header-bg);
  }
  &-profile {
    width: 32px;
    border-radius: 50%;
    object-fit: cover;
  }
  &-title {
    font-size: 18px;
    font-weight: 600;
  }
  &-main {
    flex-grow: 1;
  }
}

.chat-msg-img {
  height: 40px;
  width: 40px;
  border-radius: 50%;
  object-fit: cover;
}

.chat-msg-profile {
  flex-shrink: 0;
  margin-top: auto;
  margin-bottom: -20px;
  position: relative;
}

.chat-msg-date {
  position: absolute;
  left: calc(100% + 12px);
  bottom: 0;
  font-size: 12px;
  font-weight: 600;
  color: var(--msg-date);
  white-space: nowrap;
}

.chat-msg {
  display: flex;
  padding: 0 20px 45px;
  &-content {
    margin-left: 12px;
    max-width: 70%;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
  }
  &-text {
    background-color: var(--chat-text-bg);
    padding: 15px;
    border-radius: 20px 20px 20px 0;
    line-height: 1.5;
    font-size: 14px;
    font-weight: 500;
    & + & {
      margin-top: 10px;
    }
  }
}

.chat-msg-text {
  color: var(--chat-text-color);
}

.owner {
  flex-direction: row-reverse;
  .chat-msg-content {
    margin-left: 0;
    margin-right: 12px;
    align-items: flex-end;
  }
  .chat-msg-text {
    background-color: var(--theme-color);
    color: #fff;
    border-radius: 20px 20px 0 20px;
  }
  .chat-msg-date {
    left: auto;
    right: calc(100% + 12px);
  }
}

.chat-msg-text img {
  max-width: 300px;
  width: 100%;
}

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
}

.chat-area-footer svg {
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

.chat-area-footer input {
  border: none;
  color: var(--body-color);
  background-color: var(--input-bg);
  padding: 12px;
  border-radius: 6px;
  font-size: 15px;
  margin: 0 12px;
  width: 100%;
  &::placeholder {
    color: var(--input-chat-color);
  }
}
</style>