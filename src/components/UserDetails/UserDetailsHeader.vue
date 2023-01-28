<template>
  <div class="detail-area-header">
    <div class="msg-profile group">
      <svg viewBox="0 0 24 24" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round" stroke-linejoin="round" class="css-i6dzq1">
        <path d="M12 2l10 6.5v7L12 22 2 15.5v-7L12 2zM12 22v-6.5" />
        <path d="M22 8.5l-10 7-10-7" />
        <path d="M2 15.5l10-7 10 7M12 2v6.5" /></svg>
    </div>
    <div class="detail-title">CodePen Group</div>
    <div class="detail-subtitle">Created by Aysenur, 1 May 2020</div>
    <div class="detail-buttons">
      <button class="detail-button">
        <svg viewbox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" fill="currentColor" stroke="currentColor" stroke-width="0" stroke-linecap="round" stroke-linejoin="round" class="feather feather-phone">
          <path d="M22 16.92v3a2 2 0 01-2.18 2 19.79 19.79 0 01-8.63-3.07 19.5 19.5 0 01-6-6 19.79 19.79 0 01-3.07-8.67A2 2 0 014.11 2h3a2 2 0 012 1.72 12.84 12.84 0 00.7 2.81 2 2 0 01-.45 2.11L8.09 9.91a16 16 0 006 6l1.27-1.27a2 2 0 012.11-.45 12.84 12.84 0 002.81.7A2 2 0 0122 16.92z" />
        </svg>
        Call Group
      </button>
      <button class="detail-button">
        <svg viewbox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" fill="currentColor" stroke="currentColor" stroke-width="0" stroke-linecap="round" stroke-linejoin="round" class="feather feather-video">
          <path d="M23 7l-7 5 7 5V7z" />
          <rect x="1" y="5" width="15" height="14" rx="2" ry="2" /></svg>
        Video Chat
      </button>
    </div>
  </div>
</template>

<style scoped lang="scss">
.detail-area-header {
  display: flex;
  flex-direction: column;
  align-items: center;

  .msg-profile {
    margin-right: 0;
    width: 60px;
    height: 60px;
    margin-bottom: 15px;
  }
}

.detail-title {
  font-size: 18px;
  font-weight: 600;
  margin-bottom: 10px;
}

.detail-subtitle {
  font-size: 12px;
  font-weight: 600;
  color: var(--msg-date);
}

.detail-button {
  border: 0;
  background-color: var(--button-bg-color);
  padding: 10px 14px;
  border-radius: 5px;
  color: var(--button-color);
  display: flex;
  flex-flow: column;
  align-items: center;
  justify-content: center;
  font-size: 14px;
  flex-grow: 1;
  font-weight: 500;
  svg {
    width: 25px;
    height: 30px;
    margin-right: 10px;
  }
  &:last-child {
    margin-left: 8px;
  }
}

.detail-buttons {
  margin-top: 20px;
  display: flex;
  width: 100%;
}
</style>
