# 第二次课题

Vue 生命周期钩子 + 路由导航守卫

## 课题目标

1. Vue 生命周期钩子函数和基本用法
2. router 路由导航守卫和基本用法
3. 组件之间生命周期执行顺序
4. mixin 混入的生命周期钩子执行
5. watch 和 computed 的触发时机

### Vue 生命周期钩子函数和基本用法
### router 路由导航守卫和基本用法

### 组件之间生命周期执行顺序
加载渲染过程  
`父beforeCreate->父created->父beforeMount->子beforeCreate->子created->子beforeMount->子mounted->父mounted`  
销毁过程  
`父beforeDestroy->子beforeDestroy->子destroyed->父destroyed`  

### mixin 混入的生命周期钩子执行

### watch 和 computed 的触发时机
`watch -> beforeUpdate -> computed -> update`