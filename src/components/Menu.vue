<template>
  <div id="menu">
    <nav>
      <ul>
        <li><a href="#about-me">About Me</a></li>
        <li><a href="#resume">Resume</a></li>
        <li><a href="#portfolio">Portfolio</a></li>
        <li><a href="#goals">Goals</a></li>
        <li><a href="#progresses">Progresses</a></li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
    name: 'Menu'
}
</script>

<style lang="less">
#grids {
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
}
</style>
