<template>
  <div>
    <h5>Count组件</h5>
    <p>当前值为：{{ num }}</p>
    <button @click="num += 1">点击</button>


    <button @click="show">打印 this</button>
  </div>
</template>

<script>
export default {
    // props 自定义属性 是'只读'属性 不建议修改
    // 用来设定初始值 然后把 props 的值赋值给 data 中的值
    props:{
        init:{
            // default 属性用于设置默认值
            default: 0,
            // type 属性用于规定数据类型
            type: Number,
            // required 必填项校验，必须给该自定义属性赋值，否则报错
            required: true
        }
    },
    data(){
        return {
            num: this.init
        }
    },
    methods: {
        show(){
            console.log(this)
        }
    },
}
</script>

<style lang="less">

</style>