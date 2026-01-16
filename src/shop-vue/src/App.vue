<template>
  <el-container class="layout-container-demo">
    <el-aside width="200px">
      <el-scrollbar>
        <div class="logo">Vue3 + WebApi 项目</div>
        <el-menu :default-openeds="['1','2', '3']"
        active-text-color="#ffd04b"
        background-color="#545c64"
        text-color="#fff"
        :router="true"
        >
          <el-sub-menu index="1">
            <template #title>
              <el-icon><message /></el-icon>二手店铺管理
            </template>
            <el-menu-item-group>
              <!-- <template #title>Group 1</template> -->
              <el-menu-item index="/"><el-icon><HomeFilled /></el-icon>首页</el-menu-item>
              <el-menu-item index="/category"><el-icon><Management /></el-icon>物品分类管理</el-menu-item>
              <el-menu-item index="1-3"><el-icon><List /></el-icon>二手商品管理</el-menu-item>
            </el-menu-item-group>

          </el-sub-menu>
          <el-sub-menu index="2">
            <template #title>
              <el-icon><OfficeBuilding /></el-icon>业务菜单
            </template>
            <el-menu-item-group>
              <el-menu-item index="2-1">业务 1</el-menu-item>
              <el-menu-item index="2-2">业务 2</el-menu-item>
            </el-menu-item-group>
            <el-menu-item-group>
              <el-menu-item index="2-3">业务 3</el-menu-item>
            </el-menu-item-group>
            <el-sub-menu index="2-4">
              <template #title>业务 4</template>
              <el-menu-item index="2-4-1">Option 4-1</el-menu-item>
            </el-sub-menu>
          </el-sub-menu>
          <el-sub-menu index="3">
            <template #title>
              <el-icon><setting /></el-icon>系统设置
            </template>
            <el-menu-item-group>
              <el-menu-item index="3-3"><el-icon><DataAnalysis /></el-icon>数据字典</el-menu-item>
            </el-menu-item-group>
            <el-sub-menu index="3-4">
              <template #title><el-icon><User /></el-icon>用户管理</template>
              <el-menu-item index="3-4-1"><el-icon><Place /></el-icon>修改信息</el-menu-item>
            </el-sub-menu>
          </el-sub-menu>
        </el-menu>
      </el-scrollbar>
    </el-aside>

    <el-container>
      <el-header style="text-align: right; font-size: 12px">
        <div class="toolbar">
          <el-dropdown>
            <el-icon style="margin-right: 8px; margin-top: 1px">
              <setting />
            </el-icon>
            <template #dropdown>
              <el-dropdown-menu>
                <el-dropdown-item>View</el-dropdown-item>
                <el-dropdown-item>Add</el-dropdown-item>
                <el-dropdown-item>Delete</el-dropdown-item>
              </el-dropdown-menu>
            </template>
          </el-dropdown>
          <span>Tom</span>
        </div>
      </el-header>

      <el-main>
        <router-view></router-view>
        <!-- <el-scrollbar>
          <el-table :data="tableData">
            <el-table-column prop="date" label="Date" width="140" />
            <el-table-column prop="name" label="Name" width="120" />
            <el-table-column prop="address" label="Address" />
          </el-table>
        </el-scrollbar> -->
      </el-main>
      <el-footer>Footer</el-footer>
    </el-container>
  </el-container>
</template>

<script setup>
// import router from './router';


</script>

<style scoped>
.logo {
  height: 60px;
  width: 200px;
  color: #fff;
  line-height: 60px;
  text-align: center;
  font-size: 18px;
  font-weight: bold;
  background-color: var(--el-color-primary);
  /* margin-bottom: 20px; */
}
/* .layout-container-demo{
  //height: 90vh;
} */
.layout-container-demo .el-header {
  position: relative;
  background-color: white;
  color: var(--el-text-color-primary);
  box-shadow: var(--el-box-shadow-dark);
}
.layout-container-demo .el-aside {
  color: var(--el-text-color-primary);
  background: "#545c64";
}
.layout-container-demo .el-menu {
  border-right: none;
}
.layout-container-demo .el-main {
  padding: 0;
  box-shadow: var(--el-box-shadow-dark);
  margin: 10px 0px;
}
.layout-container-demo .toolbar {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  height: 100%;
  right: 20px;
}
.el-footer { 
  text-align: center;
  color: var(--el-text-color-secondary);
  line-height: 60px;
  background-color: var(--el-bg-color-light);
  box-shadow: var(--el-box-shadow-dark);
}
</style>