<template>
  <div id="header">
    <header>T. Matsudate's Profile</header>
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
        grid-row: 1;
        grid-column-start: 1;
        grid-column-end: 3;
        background-color: hsl(90,80%,40%);
        color: hsl(0,100%,100%);

        header {
            font-size: 200%;
            font-weight: bold;
            font-style: normal;
            padding: 0.5em;
        }
    }
}
</style>
