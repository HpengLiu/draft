<template>
  <div id="app" style="text-align:center">
    <!-- <el-row :gutter="10" type="flex" justify="center">
      <el-col :span="16" :xs='2'><div>1008611111</div></el-col>
      <el-col :span="4" :xs="16"><div>1001010086</div></el-col>
      <el-col :span="4" :xs='6'><div>1000010010</div></el-col>
    </el-row>-->

    <el-container>
      <el-header height="60px">
        <el-row>
          <el-col :span="6" style="font-size:20px">我是logo</el-col>
          <el-col :span="3" offset="9">首页</el-col>
          <el-col :span="3">关于</el-col>
          <el-col :span="3">我的</el-col>
        </el-row>
      </el-header>
    </el-container>

    <el-container>
      <el-aside>
        <el-menu :default-active="activeIndex" class="el-menu-demo" @select="handleSelect">
          <el-menu-item index="1">处理中心</el-menu-item>
          <!-- 生成子菜单 -->
          <el-submenu index="2">
            <template slot="title">我的工作台</template>
            <el-menu-item-group>
              <template slot="title">你好呀</template>
              <el-menu-item index="2-1">选项1</el-menu-item>
            </el-menu-item-group>
            <el-menu-item index="2-2">选项2</el-menu-item>
            <el-menu-item index="2-3">选项3</el-menu-item>
            <el-submenu index="2-4">
              <template slot="title">选项4</template>
              <el-menu-item index="2-4-1">选项1</el-menu-item>
              <el-menu-item index="2-4-2">选项2</el-menu-item>
              <el-menu-item index="2-4-3">选项3</el-menu-item>
            </el-submenu>
          </el-submenu>
          <el-menu-item index="3" disabled>消息中心</el-menu-item>
          <el-menu-item index="4">
            <a href="https://www.ele.me" target="_blank">订单管理</a>
          </el-menu-item>
        </el-menu>
      </el-aside>
      <el-main>
        <el-header style="font-size:18px;border-radius: 30px">副标题</el-header>
        <el-button type="primary">点我</el-button>
        <el-button type="info">点我</el-button>
        <el-button type="danger" icon="el-icon-search">点我</el-button>
        <div>
          <el-button-group>
            <el-button type="danger" size="mini">上一页</el-button>
            <el-button type="danger" size="small">下一页</el-button>
            <el-button type="danger" :loading="true" size="medium">加载中</el-button>
          </el-button-group>
        </div>
        <el-link type="primary" disabled>点我</el-link>
      </el-main>
    </el-container>
    <el-container>
      <el-footer>footer</el-footer>
    </el-container>
  </div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {
      activeIndex: "1",
      activeIndex2: "1"
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    }
  },
  components: {}
};
</script>

<style lang='scss'>
.el-container {
  border: 1px solid;
  display: flex;
  // line-height: 1.7;
}
.el-header {
  background: #409eff;
  line-height: 60px;
  color: white;
}
.el-aside {
  background: #e6a23c;
  border: 1px solid;
  height: 600px;
}
.el-main {
  // background:#9ed900;
  background: #67c23a;
}
.el-footer {
  background: #f56c6c;
}
.el-col {
  // border: 1px solid;
  color: white;
}
</style>

