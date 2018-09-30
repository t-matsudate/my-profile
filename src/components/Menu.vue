<template>
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
