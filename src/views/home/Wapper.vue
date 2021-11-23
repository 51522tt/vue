<template>
  <div class="home">
    <div class="position">
      <span class="iconfont position__icon">&#xe651;</span>
      北京理工大学国防科技园2号楼10层
      <span class="iconfont position__notice">&#xe69f;</span>
    </div>
    <Search id='search'/>
    <Banner id='banner'/>
    <Features id='Features'/>
    <div class="gap"></div>
    <Nearby id='nearby'/>

  </div>
</template>

<script>
import Search from '../../components/Search.vue'
import Banner from '../../components/Banner.vue'
import Features from '../../components/Features.vue'
import Nearby from '../../components/Nearby.vue'
export default {
  name: 'Wapper',
  components: {
    Search,
    Banner,
    Features,
    Nearby
  }
}

</script>

<style lang='scss'>
@import '../../style/mixins.scss';
#menu {
  position:absolute;
  bottom: 0;
  width:100%;
  height: 0.49rem;
}
.home{
  padding:0 .18rem .3rem;
  overflow-y:auto
}
.gap{
    margin: 0 -.18rem;
    background-color: #F1F1F1;
    height: 0.1rem;
  }
#search{
  margin-bottom: .12rem;
}
#banner{
  margin-bottom: 0.16rem;
}

.position {
  position: relative;
  padding: 0.16rem .24rem .16rem 0;
  line-height: 0.22rem;
  font-size: 0.16rem;
  @include ellipsis;
  .position__icon{
    position: relative;
    font-size: 0.2rem;
    top:0.01rem;
  }
  .position__notice {
    position: absolute;
    right: 0;
    top:0.174rem;
    font-size: 0.2rem;
  }
}
</style>
