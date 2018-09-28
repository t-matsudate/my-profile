<template>
  <div id="grids">
    <div id="header">
      <header>Func's Profile</header>
    </div>
    <div id="menu">
      <nav>
        <ul>
          <li>About Me</li>
          <li>Resume</li>
          <li>Portfolio</li>
          <li>Goals</li>
          <li>Progresses</li>
        </ul>
      </nav>
    </div>
    <div id="main">
      <main>Test</main>
    </div>
  </div>
</template>

<script>
export default {
    name: 'GridMenu'
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

    #header {
        grid-row: 1;
        grid-column-start: 1;
        grid-column-end: 3;
        background-color: rgb(32,32,32);


        header {
            font-size: 200%;
            font-weight: bold;
            font-style: normal;
            padding: 0.5em;
        }
    }

    #menu {
        grid-row: 2;
        grid-column: 1;
        background-color: rgb(64,64,64);

        nav {
            li {
                font-size: 150%;
                font-weight: bold;
                font-style: normal;
                padding: 0.5em;
            }
        }
    }

    #main {
        grid-row: 2;
        grid-column: 2;
        
        main {
            padding: 1em;
        }
    }
}
</style>
