
<script setup>
import MessageArea from './MessageArea.vue'
</script>

<template>
  <div class="chat-area">
    <div class="chat-area-header">
      <div class="chat-area-title">CodePen Group</div>
      <div class="chat-area-group">
        <img class="chat-area-profile" src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/3364143/download+%283%29+%281%29.png" alt="" />
        <img class="chat-area-profile" src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/3364143/download+%282%29.png" alt="">
        <img class="chat-area-profile" src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/3364143/download+%2812%29.png" alt="" />
        <span>+4</span>
      </div>
    </div>
    <v-card class="chat-area-main">
      <v-row>
        <v-col
          cols="12"
        >
          <div class="chat-msg">
            <div class="chat-msg-profile">
              <img class="chat-msg-img" src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/3364143/download+%283%29+%281%29.png" alt="" />
              <div class="chat-msg-date">Message seen 1.22pm</div>
            </div>
            <div class="chat-msg-content">
              <div class="chat-msg-text">Luctus et ultrices posuere cubilia curae.</div>
              <div class="chat-msg-text">
                <img src="https://media0.giphy.com/media/yYSSBtDgbbRzq/giphy.gif?cid=ecf05e47344fb5d835f832a976d1007c241548cc4eea4e7e&rid=giphy.gif" /></div>
              <div class="chat-msg-text">Neque gravida in fermentum et sollicitudin ac orci phasellus egestas. Pretium lectus quam id leo.</div>
            </div>
          </div>
        </v-col>
        <v-col  cols="12">
          <div class="chat-msg owner">
            <div class="chat-msg-profile">
              <img class="chat-msg-img" src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/3364143/download+%281%29.png" alt="" />
              <div class="chat-msg-date">Message seen 1.22pm</div>
            </div>
            <div class="chat-msg-content">
              <div class="chat-msg-text">Sit amet risus nullam eget felis eget. Dolor sed viverra ipsum😂😂😂</div>
              <div class="chat-msg-text">Cras mollis nec arcu malesuada tincidunt.</div>
            </div>
          </div>
        </v-col>
        <v-col  cols="12">
          <div class="chat-msg">
            <div class="chat-msg-profile">
              <img class="chat-msg-img" src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/3364143/download+%282%29.png" alt="">
              <div class="chat-msg-date">Message seen 2.45pm</div>
            </div>
            <div class="chat-msg-content">
              <div class="chat-msg-text">Aenean tristique maximus tortor non tincidunt. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae😊</div>
              <div class="chat-msg-text">Ut faucibus pulvinar elementum integer enim neque volutpat.</div>
            </div>
          </div>
        </v-col>
        <v-col  cols="12">
          <div class="chat-msg owner">
            <div class="chat-msg-profile">
              <img class="chat-msg-img" src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/3364143/download+%281%29.png" alt="" />
              <div class="chat-msg-date">Message seen 2.50pm</div>
            </div>
            <div class="chat-msg-content">
              <div class="chat-msg-text">posuere eget augue sodales, aliquet posuere eros.</div>
              <div class="chat-msg-text">Cras mollis nec arcu malesuada tincidunt.</div>
            </div>
          </div>
        </v-col>
        <v-col  cols="12">
          <div class="chat-msg">
            <div class="chat-msg-profile">
              <img class="chat-msg-img" src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/3364143/download+%2812%29.png" alt="" />
              <div class="chat-msg-date">Message seen 3.16pm</div>
            </div>
            <div class="chat-msg-content">
              <div class="chat-msg-text">Egestas tellus rutrum tellus pellentesque</div>
            </div>
          </div>
        </v-col>
        <v-col  cols="12">
          <div class="chat-msg">
            <div class="chat-msg-profile">
              <img class="chat-msg-img account-profile" src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/3364143/download+%283%29+%281%29.png" alt="">
              <div class="chat-msg-date">Message seen 3.16pm</div>
            </div>
            <div class="chat-msg-content">
              <div class="chat-msg-text">Consectetur adipiscing elit pellentesque habitant morbi tristique senectus et.</div>
            </div>
          </div>
        </v-col>
        <v-col  cols="12">
          <div class="chat-msg owner">
            <div class="chat-msg-profile">
              <img class="chat-msg-img" src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/3364143/download+%281%29.png" alt="" />
              <div class="chat-msg-date">Message seen 2.50pm</div>
            </div>
            <div class="chat-msg-content">
              <div class="chat-msg-text">Tincidunt arcu non sodales😂</div>
            </div>
          </div>
        </v-col>
        <v-col  cols="12">
          <div class="chat-msg">
            <div class="chat-msg-profile">
              <img class="chat-msg-img" src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/3364143/download+%282%29.png" alt="">
              <div class="chat-msg-date">Message seen 3.16pm</div>
            </div>
            <div class="chat-msg-content">
              <div class="chat-msg-text">Consectetur adipiscing elit pellentesque habitant morbi tristique senectus et🥰</div>
            </div>
          </div>
        </v-col>
      </v-row>
    </v-card>
    <MessageArea />
  </div>
</template>


<style scoped lang="scss">
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
      overflow-y: auto;
      max-height: calc(100vh - 220px);
    }

    &-group {
      flex-shrink: 0;
      display: flex;

      * {
        border: 2px solid var(--theme-bg-color);
      }

      * + * {
        margin-left: -5px;
      }

      span {
        width: 32px;
        height: 32px;
        background-color: var(--button-bg-color);
        color: var(--theme-color);
        border-radius: 50%;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 14px;
        font-weight: 500;
      }
    }
  }

  .chat-msg{
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
      color: var(--chat-text-color);
      background-color: var(--chat-text-bg);
      padding: 15px;
      border-radius: 20px 20px 20px 0;
      line-height: 1.5;
      font-size: 14px;
      font-weight: 500;

      & img {
        max-width: 300px;
        width: 100%;
      }

      & + & {
        margin-top: 10px;
      }
    }

    &-img {
      height: 40px;
      width: 40px;
      border-radius: 50%;
      object-fit: cover;
    }

    &-profile {
      flex-shrink: 0;
      margin-top: auto;
      margin-bottom: -20px;
      position: relative;
    }

    &-date {
      position: absolute;
      left: calc(100% + 12px);
      bottom: 0;
      font-size: 12px;
      font-weight: 600;
      color: var(--msg-date);
      white-space: nowrap;
    }
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
</style>
