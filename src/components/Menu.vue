<template>
  <div id="menu" class="hidden">
    <MenuBar />
    <div id="menu-list">
      <nav>
        <ul>
          <li><a href="#about-me">T.Matsudateについて</a></li>
          <li><a href="#resume">履歴</a></li>
          <li><a href="#portfolio">ポートフォリオ</a></li>
          <li><a href="#goals">到達目標</a></li>
          <li><a href="#progresses">開発の進捗状況</a></li>
          <li><a href="#donate">寄付等について</a></li>
        </ul>
      </nav>
    </div>
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
        overflow-y: scroll;
        width: 50%;
        background-color: hsl(90, 50%, 99%);

        .menu-bar {
            padding: 1em;

            a {
                .fas {
                    font-size: 200%;
                    color: hsl(90,80%,40%);
                }
            }
        }

        #menu-list {
            nav {
                li {
                    font-size: 100%;
                    font-weight: normal;
                    font-style: normal;
                    padding: 0.5em;

                    a {
                        color: hsl(0,0%,0%);
                        text-decoration: none;
                    }
                }
            }
        }
    }

    #menu.hidden {
        display: none;
    }

    #menu.shown {
        display: block;
    }
}
</style>
