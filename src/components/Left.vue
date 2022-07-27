<template>
  <div class="left-container">
    <h3>Left 组件</h3>
    <hr>
    <MyCount :init="6"></MyCount>
  </div>
</template>

<script>
</script>

<!-- scoped 给该组件每个元素添加自定义属性 -->
<!-- 通过属性选择器修改样式 避免当前style影响其它组件 -->
<style lang="less" scoped>
  .left-container {
    padding: 0 20px 20px;
    background-color: orange;
    min-height: 250px;
    flex: 1;
  }
  // [data-v-01] 属性选择器
  h3{
    color: red;
  }

  // /deep/ 就对应了当前组件的自定义属性值
  // /deep/ h5 => [data-v-3c83f0b7] h5 所以能影响到子组件
  // 简单来说，它可以修改子组件的样式 
  /deep/ h5{
    color: pink;
  }
</style>

