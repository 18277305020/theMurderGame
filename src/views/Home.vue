<template>
  <div class="main-box">
    <!-- 操作菜单栏 -->
    <div>
      <MenuBar></MenuBar>
    </div>
    <!-- 好友列表 -->
    <div>
      <PlayerList></PlayerList>
    </div>
    <!-- 聊天室 -->
    <div class="room">
      <ChatRoom></ChatRoom>
    </div>
  </div>
</template>

<script>
import MenuBar from "@/components/MenuBar";
import PlayerList from "@/components/PlayerList";
import ChatRoom from "@/components/ChatRoom";

export default {
  components: {
    MenuBar,
    PlayerList,
    ChatRoom
  },
  name: "Home"
};
</script>

<style lang="less" scoped>
.main-box{
  display: flex;
}

.room{
  flex: 1;
}
</style>
