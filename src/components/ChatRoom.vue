<template>
  <div class="room">
    <div class="hand-box">
      <h2>灵魂频道 ( 4 )</h2>
      <div class="plans">
        <Avatar
          class="plans-user"
          size="40"
          src="https://i.loli.net/2017/08/21/599a521472424.jpg"
          v-for="i in 20"
          :key="i.id"
        />
      </div>
    </div>

    <div class="conten">
      <div>
        <div v-for="i in 10" :key="i.id">
          <div class="item">
            <div>
              <Avatar size="40" src="https://i.loli.net/2017/08/21/599a521472424.jpg" />
            </div>
            <div class="item-content">
              <h4>lisa</h4>
              <div
                class="text"
              >asdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasd</div>
            </div>
          </div>

          <div class="item-rigth">
            <div>
              <Avatar size="40" src="https://i.loli.net/2017/08/21/599a521472424.jpg" />
            </div>
            <div class="item-content-right">
              <div
                class="text-right"
              >asdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdasdad</div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="send-box">
      <Input v-model="textareaValue" type="textarea" :rows="4" placeholder="请输入要发送的内容..." />
      <Button class="button" type="primary">发送</Button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      textareaValue: ""
    };
  }
};
</script>

<style lang="less" scoped>
.room {
  display: flex;
  flex-direction: column;

  width: 100%;
  height: 100vh;
  background-image: linear-gradient(#606d96, #383d45);

  position: relative;
  z-index: 100;
  box-shadow: 40px 0px 100px #000;
}

.hand-box {
  text-align: center;
  padding: 20px 0 0;

  position: relative;
  box-shadow: 10px -20px 100px #000;

  color: white;
}

.conten {
  flex: 1;
  overflow: auto;
}

.send-box {
  width: 100%;
  height: 200px;
  padding: 40px;
  box-shadow: 100px 40px 100px #000;

  text-align: right;
}

.button {
  margin-top: 10px;
}

.item {
  display: flex;
  padding: 20px 40px;
  color: white;
}

.item-rigth {
  display: flex;
  flex-direction: row-reverse;
  padding: 20px 40px;
  color: white;
  text-align: right;
}

.item-content {
  margin-left: 20px;
  width: 60%;
  word-wrap: break-word;
  word-break: break-all;
  overflow: hidden;
}

.item-content-right {
  margin-right: 20px;
  width: 60%;
  word-wrap: break-word;
  word-break: break-all;
  overflow: hidden;
}

.text {
  margin-top: 10px;
  padding: 20px;
  background: rgba(0, 0, 0, 0.2);
}

.text-right {
  margin-top: 10px;
  padding: 20px;
  background-image: linear-gradient(#60a7de, #60ace1);
}

.plans {
  border-top: 1px solid #6b79a4;
  padding: 20px;
  margin-top: 20px;
  text-align: left;
}

.plans-user {
  margin: 0 10px 10px;
}
</style>