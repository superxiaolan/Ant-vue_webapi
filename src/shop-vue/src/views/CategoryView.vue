<template>
  <el-card style="max-width: 600px">
        <template #header>
          <span>商品分类</span>
          <el-button type="primary" icon="CirclePlus" round>添加分类</el-button>
        </template>
        <el-table :data="tableData" stripe style="width: 100%">
        <el-table-column prop="id" label="Id" width="120" />
        <el-table-column prop="name" label="名称" width="120" />
        <el-table-column prop="address" label="Address" width="180"/>
        <el-table-column fixed="right" label="Operations" min-width="180">
        <!-- 固定列 -->
      <template #default>
        <el-button type="primary" size="small" @click="handleClick">
          编辑
        </el-button>
        <el-button type="danger" size="small">删除</el-button>
      </template>
    </el-table-column>
        </el-table>
  </el-card>
        
</template>

<script setup>
const tableData = [
  {
    id: '2016-05-03',
    name: 'Tom',
    address: 'No. 189, Grove St, Los Angeles',
  },
  {
    id: '2016-05-02',
    name: 'Tom',
    address: 'No. 189, Grove St, Los Angeles',
  },
  {
    id: '2016-05-04',
    name: 'Tom',
    address: 'No. 189, Grove St, Los Angeles',
  },
  {
    id: '2016-05-01',
    name: 'Tom',
    address: 'No. 189, Grove St, Los Angeles',
  },
]
</script>