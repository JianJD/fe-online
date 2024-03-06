<template>
  <div class="flexCls-align">
   <org-tree></org-tree>
   <user-table></user-table>
  </div>
</template>

<script setup lang="ts">
import OrgTree from "./components/OrgTree.vue"
import UserTable from "./components/UserTable.vue"
</script>
<style scoped lang="less">
.flexCls-align {
  display: flex;
  gap:20px
}

</style>
