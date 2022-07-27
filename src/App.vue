<template>
  <div class="app-container">
    <h1>App 根组件</h1>
    <h3>测试</h3>
    <hr />

    <div class="box">
      <!-- 渲染 Left 组件和 Right 组件 -->
      <Left/>
      <Right/>
    </div>
  </div>
</template>

<script>
// 注册私人组件
import Left from '@/components/Left.vue'
import Right from '@/components/Right.vue'
export default {
  data(){
    return {}
  },
  components:{
    // 全写
    'Left': Left,
    // 简写 相同的键值对
    Right
  },
  methods:{}
}
</script>

<style lang="less">
.app-container {
  padding: 1px 20px 20px;
  background-color: #efefef;
}
.box {
  display: flex;
}
</style>
