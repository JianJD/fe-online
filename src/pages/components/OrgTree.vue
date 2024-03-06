<template>
  <div class="minw-200">
    <el-tree :data="data" @node-click="nodeClick"> </el-tree>

  </div>
</template>

<script setup lang="ts">
import type Node from 'element-plus/es/components/tree/src/model/node'
interface Tree {
  label: string;
  children?: Tree[];
}
import { ref, reactive, toRefs, onMounted,defineProps,defindEmits } from "vue";
const curId = ref<number>(0);
const data = ref<Tree>([
  {
    label: "集团公司",
    children: [
      {
        label: "子公司",
        children: [
          {
            label: "技术部",
          },
        ],
      },
      {
        label: "子公司2",
        children: [
          {
            label: "技术部2",
          },
        ],
      },
    ],
  },
  
]);
function  nodeClick(_,a:Node) {
    console.log(a.data);
    
}

</script>
<style scoped lang="less">
.minw-200 {
  min-width: 200px;
}
</style>