<!--
 * @Description: 
 * @LastEditors: HL
 * @LastEditTime: 2020-03-16 16:53:36
 -->
<template>
  <div class="adesk-affix-demo">
    <p class="test"
       v-for="item in list"
       :key="'p1_'+item">为了测试</p>
    <Affix :offset-top="50">
      <span class="demo-affix">固定在顶部50px</span>
    </Affix>
    <Affix :offset-bottom="50">
      <span class="demo-affix">固定在底部50px</span>
    </Affix>
    <p class="test"
       v-for="item in list"
       :key="'p2_'+item">为了测试</p>
  </div>
</template>
<script>
import Affix from "../packages/affix/index";
export default {
  data() {
    return {
      list: [1, 2, 3, 4, 5, 6, 7, 8]
    };
  },

  components: {
    Affix
  },

};
</script>
<style scoped lang="less">
.test {
  line-height: 80px;
}
.demo-affix {
  background-color: blue;
}

</style>
