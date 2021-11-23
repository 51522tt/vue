<template>
  <Wapper id='wapper'/>
  <Menu id='menu'/>
</template>

<script>
import Wapper from './Wapper.vue'
import Menu from '../../components/Menu.vue'
export default {
  name: 'Home',
  components: {
    Wapper,
    Menu
  }
}

</script>

<style lang='scss'>
@import '../../style/mixins.scss';

#wapper {
  position:absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: .49rem;
}
#menu {
  position:absolute;
  bottom: 0;
  width:100%;
  height: 0.49rem;
}
</style>
