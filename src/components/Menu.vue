<template>
  <div id="menu" class="menu-hidden">
    <nav>
      <MenuBar />
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
import MenuBar from './MenuBar.vue'

export default {
    name: 'Menu',
    components: {
        MenuBar
    }
}
</script>

<style lang="less">
#grids {
    #menu {
        z-index: 2;
        position: fixed;
        top: 0;
        bottom: 0;
        width: 20%;
        background-color: hsl(90, 50%, 95%);

        nav {
            .menu-bar {
                z-index: 2;
                background-color: hsl(90,50%,95%);

                a {
                    .fas {
                        margin: 0.5em;
                        font-size: 200%;
                        color: hsl(90,80%,40%);
                    }
                }
            }

            li {
                font-size: 100%;
                font-weight: normal;
                font-style: normal;
                padding: 0.5em;
            }
        }

        a {
            color: hsl(0,0%,0%);
            text-decoration: none;
        }
    }

    #menu-shown {
        display: block;
    }

    #menu-hidden {
        display: none;
    }
}
</style>
