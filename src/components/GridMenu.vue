<template>
  <div id="grids">
    <Header />
    <Menu />
    <Main />
  </div>
</template>

<script>
import Header from './Header.vue'
import Menu from './Menu.vue'
import Main from './Main.vue'

export default {
    name: 'GridMenu',
    components: {
      Header,
      Menu,
      Main
    }
}
</script>

<style lang="less">
@menu-width: 20%;

* {
  margin: 0;
  padding: 0;
}

#grids {
    display: grid;
    grid-template-rows: repeat(2, auto);
    grid-template-columns: @menu-width 100% - @menu-width;

    a {
        color: hsl(0,0%,0%);
    }
}
</style>
