<template>
  <div class="list-box">
    <div class="search-box">
      <Input search placeholder="查找好友" />
    </div>
    <div class="item">
      <div
        @click="onItem(index)"
        class="item-box"
        v-for="(i,index) in 20"
        :key="i.id"
        :class="indext === index?'item-bg':null"
      >
        <div>
          <Badge :count="1">
            <Avatar
              shape="square"
              size="50"
              icon="ios-person"
              src="https://i.loli.net/2017/08/21/599a521472424.jpg"
            />
          </Badge>
        </div>
        <div class="conten">
          <h2>lisa</h2>
          <h4>聊天内容聊天内容聊天内容聊天内容聊天内容聊天内容聊天内容聊天内容聊天内容聊天内容</h4>
        </div>
        <h4>12:00</h4>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      indext: 0
    };
  },
  methods: {
    onItem(index) {
      this.indext = index;
    }
  }
};
</script>

<style lang="less" scoped>
.list-box {
  width: 400px;
  background-image: linear-gradient(#606d96, #1c1e24);
}

.search-box {
  padding: 40px;
  position: relative;
  z-index: 90;
  box-shadow: -40px -40px 100px #000;
}

.item {
  height: calc(100vh - 112px);
  overflow: auto;
}

.item-box {
  padding: 20px 20px 20px 40px;

  display: flex;
  justify-content: space-between;
  align-items: center;
  cursor: pointer;
  color: white;

}

.conten {
  width: 200px;
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 1;
  overflow: hidden;
}

.item-bg {
  background: rgba(105, 85, 93, 0.4);
  transition: 0.5s;
}
</style>