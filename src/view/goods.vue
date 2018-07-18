<!--  -->
<template>
  <div class="goods">
      this is good id:
      <span>{{$route.query.goodsId}}</span>
      <br/>
      <a @click="$router.back(-1)">返回</a>
  </div>
</template>

<script>
export default {
}

</script>
<style  scoped>
</style>