<template>
    <div>
        <h1>
            坚持可持续发展战略
        </h1>
    </div>
</template>
<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: ''
    }
  },
  extends: {
    add (){
      console.log('ok')
      $store.mutations();
    }
  },
  // 局部路由根methods是一个级别
  // 组件路由进入触发
  beforeRouteEnter (to, from, next) {
    console.log('局部路由监听_组件路由进入新闻页触发')
    // console.log(this);
    // 路由进入 实例为创建
    // next({path:"/info"});
    // console.log(to,from);
    // if(from.path=="/test"){
    //   // 如果他的上一级路由是  test,直接回info
    //   next({path:"/info"})

    // }else{
    //   next()
    // }
    next()
  },
  // 子路由进入触发
  beforeRouteUpdate (to, from, next) {
    console.log('局部路由监听_进入子路由触发')
    next()
  },
  // 组件路由离开触发
  beforeRouteLeave (to, from, next) {
    console.log('局部路由监听_组件离开新闻页触发')
    next()
  }
}
</script>