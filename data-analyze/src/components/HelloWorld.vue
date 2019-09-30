<template>
  <div class="layout">
    <Layout>
      <Sider breakpoint="md" collapsible :collapsed-width="78" v-model="isCollapsed">
        <Menu active-name="1-1" theme="dark" width="auto" :class="menuitemClasses">
          <MenuItem name="1-1" class="one">
            <Icon type="ios-navigate"></Icon>
            <span>首页</span>
          </MenuItem>
          <MenuItem name="1-2" class="one">
            <Icon type="ios-navigate"></Icon>
            <span>就业地区分布统计</span>
          </MenuItem>
          <MenuItem name="1-3" class="one">
            <Icon type="ios-settings"></Icon>
            <span>就业单位统计</span>
          </MenuItem>
          <MenuItem name="1-4" class="one">
            <Icon type="ios-settings"></Icon>
            <span>就业行业统计</span>
          </MenuItem>
          <MenuItem name="1-5" class="two">
            <Icon type="ios-navigate"></Icon>
            <span>就业职业统计</span>
          </MenuItem>
        </Menu>
        <div slot="trigger"></div>
      </Sider>
      <Layout>
        <Header class="layout-header-bar">招就处数据分析系统</Header>
        <Content :style="{margin: '20px', background: '#fff', minHeight: '220px'}"></Content>
      </Layout>
    </Layout>
  </div>
</template>

<script>
export default {
  // name: 'HelloWorld',
  // data() {
  //   return {
  //     msg: 'Welcome to Your Vue.js App'
  //   }
  // }
  // data() {
  //   return {
  //     isCollapsed: false
  //   }
  // },
  // computed: {
  //   menuitemClasses: function() {
  //     return ['menu-item', this.isCollapsed ? 'collapsed-menu' : '']
  //   }
  // }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.layout {
  border: 1px solid #d7dde4;
  background: #f5f7f9;
  position: relative;
  border-radius: 4px;
  overflow: hidden;
}
.layout-header-bar {
  background: #fff;
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.1);
}
.menu-item span {
  display: inline-block;
  overflow: hidden;
  width: 69px;
  text-overflow: ellipsis;
  white-space: nowrap;
  vertical-align: bottom;
  transition: width 0.2s ease 0.2s;
}
.menu-item i {
  transform: translateX(0px);
  transition: font-size 0.2s ease, transform 0.2s ease;
  vertical-align: middle;
  font-size: 16px;
}
.collapsed-menu span {
  width: 0px;
  transition: width 0.2s ease;
}
.collapsed-menu i {
  transform: translateX(5px);
  transition: font-size 0.2s ease 0.2s, transform 0.2s ease 0.2s;
  vertical-align: middle;
  font-size: 22px;
}
.up {
  margin: 0 auto;
  padding-top: 5%;
}
.one {
  padding-top: 30%;
}
.two {
  padding-top: 30%;
  padding-bottom: 30%;
}
</style>
