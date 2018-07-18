<!--  -->
<template>
  <div class="test">
      <!--动态路由-->
      this is testId: {{$route.params.testId}}
      <br/>
      <!-- 嵌套路由-->
      <router-link to="/test/title1">标题1</router-link>
      <router-link to="/test/title2">标题2</router-link>
      <router-view></router-view>
      <br/>
      <!--编程路由-->
      <div>
          跳转到商品：
          <input type="text" v-model="input"/>
          <a @click="gotoGoods">OK</a>
      </div>
  </div>
</template>

<script>
export default {
    methods:{
        gotoGoods(){
            this.$router.push({
                path: '/goods',
                query: {
                    goodsId: this.input
                }
            });
        }
    }

}

</script>
<style  scoped>
</style>