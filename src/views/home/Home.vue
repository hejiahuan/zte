<template>
  <div class="home">
     <NavTopBar/>
     <NavHeader/>
     <Swiper/>
  </div>
</template>

<script>
//导入header
import NavTopBar from "components/common/NavTopBar";

import NavHeader from "components/common/NavHeader";

//导入Swiper
import Swiper from '@/components/common/NavSwiper'

export default {
    name:"Home",
    components:{
      NavTopBar,
      NavHeader,
      Swiper
    }
}
</script>

<style lang="scss" scoped>
</style>