<template>
  <div class="box">
    <Card :bordered="false" class="login-box">
      <p slot="title">用户登陆</p>
      <div class="form">
        <Form :model="form" :label-width="100">
          <FormItem label="用户账号">
            <Input v-model="form.account" />
          </FormItem>
          <FormItem label="用户密码">
            <Input v-model="form.password" />
          </FormItem>
        </Form>
        <div class="bth">
          <Button type="primary" @click="onLogin">登陆</Button>
          <Button type="primary">注册</Button>
        </div>
      </div>
    </Card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {}
    };
  },
  methods: {
    async onLogin() {
      const { data } = await this.$http.post("/login", this.form);
      if (data.data) {
          this.$Message.success('登陆成功');
          sessionStorage.setItem('langrenshaToken',data.data.token)
          this.$router.push('/')
      }else{
          this.$Message.error(data.message);
      }
    }
  }
};
</script>

<style lang="less" scoped>
.box {
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;

  background: url(../assets/loginBg.png) no-repeat center;
}

.login-box {
  width: 40%;
  height: 30%;
  background: #ffffff;
}

.form {
  padding: 20px 40px;
}

.bth {
  width: 100%;
  text-align: center;

  button {
    margin: 0 10px;
  }
}
</style>