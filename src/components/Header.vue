<template>
  <div id="header">
    <header>
      <h1 id="app-title">T. Matsudate's Profile</h1>
    </header>
  </div>
</template>

<script>
export default {
    name: 'Header'
}
</script>

<style lang="less">
#grids {
    #header {
        z-index: 1;
        grid-row: 1;
        grid-column: 2;
        background-color: hsl(90, 80%, 40%);
        color: hsl(90,100%,100%);

        header {
            #app-title {
                grid-column: 2;
                padding: 0.5em;
                font-size: 200%;
                font-weight: bold;
                font-style: normal;
            }
        }
    }
}
</style>
