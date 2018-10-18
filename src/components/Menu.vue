<template>
  <div id="menu">
    <nav>
      <ul>
        <li><a href="#about-me">About Me</a></li>
        <li><a href="#resume">Resume</a></li>
        <li><a href="#portfolio">Portfolio</a></li>
        <li><a href="#goals">Goals</a></li>
        <li><a href="#progresses">Progresses</a></li>
        <li><a href="#donate">Donate</a></li>
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

        background-color: hsl(90, 50%, 95%);

        nav {
            li {
              font-size: 120%;
              font-weight: bold;
              font-style: normal;
              padding: 0.5em;
            }
        }

        a {
            color: hsl(0,0%,0%);
            text-decoration: none;
        }
    }
}
</style>
