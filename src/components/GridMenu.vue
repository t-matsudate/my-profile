<template>
  <div id="grids">
    <Header />
    <Menu />
    <div id="main">
      <main>Test</main>
    </div>
  </div>
</template>

<script>
import Header from './Header.vue'
import Menu from './Menu.vue'

export default {
    name: 'GridMenu',
    components: {
      Header,
      Menu
    }
}
</script>

<style lang="less">
@header-height: 20%;
@menu-width: 20%;

* {
  margin: 0;
  padding: 0;
}

#grids {
    display: grid;
    grid-template-rows: @header-height 100% - @header-height;
    grid-template-columns: @menu-width 100% - @menu-width;

    #main {
        grid-row: 2;
        grid-column: 2;
        
        main {
            padding: 1em;
        }
    }
}
</style>
