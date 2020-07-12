<template>
  <div class="box">
    <div class="flex-box">
      <div>
        <div>
          <Badge :count="1">
            <Avatar
              size="60"
              icon="ios-person"
              src="https://i.loli.net/2017/08/21/599a521472424.jpg"
            />
          </Badge>
        </div>
        <div class="mag-top">
          <Badge :count="1">
            <Icon size="40" type="ios-chatboxes-outline" style="color:#fff" />
          </Badge>
        </div>
      </div>

      <div>
        <div class="icon">
          <Icon type="logo-windows" size="24" />
        </div>

        <div class="mag-top-min icon">
          <Icon type="md-reorder" size="24" />
        </div>

        <div class="mag-top-min icon">
          <Icon type="ios-apps" size="24" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="less" scoped>
.flex-box {
  box-shadow: -40px 0px 100px #000;
  width: 140px;
  height: 100vh;
  padding: 40px 0;
  display: flex;
  flex-direction: column;
  justify-content: space-between;

  background-image: linear-gradient(#606d96, #383d45);
  text-align: center;

  position: relative;
  z-index: 100;
}

.mag-top {
  margin-top: 40px;
}

.mag-top-min {
  margin-top: 20px;
}

.icon {
  color: #797f92;
}
</style>