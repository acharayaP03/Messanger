<template>

</template>

<style scoped lang="scss">
  .chat-area-header {
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
      overflow-y: auto;
      max-height: calc(100vh - 220px);
    }
  }


</style>