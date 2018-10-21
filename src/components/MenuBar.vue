<template>
  <div class="menu-bar">
    <a @click="slideSideMenu"><i class="fas fa-bars"></i></a>
  </div>
</template>

<script>
export default {
    name: 'MenuBar',
    methods: {
        slideSideMenu: function() {
            let menu = document.getElementById("menu");

            if (menu.getAttribute("class") === "menu-hidden") {
                menu.setAttribute("class", "menu-shown");
            } else if (menu.getAttribute("class") === "menu-shown") {
                menu.setAttribute("class", "menu-hidden");
            } else {
                return;
            }
        }
    }
}
</script>

<style lang="less">
#grids {
    .menu-bar {
        z-index: 1;
        grid-row: 1;
        grid-column: 1;
        background-color: hsl(90, 80%, 40%);

        a {
            .fas {
                margin: 0.5em;
                font-size: 200%;
                color: hsl(90,100%,100%);
            }
        }
    }
}
</style>
