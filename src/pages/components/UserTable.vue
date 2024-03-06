<template>
  <el-table :data="tableData" style="width: 100%">
    <el-table-column prop="id" label="用户id" width="180" />
    <el-table-column prop="name" label="姓名" width="180" />
    <el-table-column prop="phone" label="手机号" />
  </el-table>
</template>

<script setup lang="ts">
import { ref, reactive, toRefs, onMounted,} from 'vue'
import { User } from '@/api/user'
const tableData =ref<User>([])
</script>
<style scoped lang="less">
</style>