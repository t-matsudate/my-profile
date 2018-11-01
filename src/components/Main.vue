<template>
  <div id="main">
    <main>
      <article>
        <AboutMe />
        <Resume />
        <Portfolio />
        <Goals />
        <Progresses />
        <Donate />
      </article>
    </main>
  </div>
</template>

<script>
import AboutMe from './main/AboutMe.vue'
import Resume from './main/Resume.vue'
import Portfolio from './main/Portfolio.vue'
import Goals from './main/Goals.vue'
import Progresses from './main/Progresses.vue'
import Donate from './main/Donate.vue'

export default {
    name: 'Main',
    components: {
        AboutMe,
        Resume,
        Portfolio,
        Goals,
        Progresses,
        Donate
    }
}
</script>

<style lang="less">
#grids {
    #main {
        z-index: 0;
        margin-top: 3em;
        grid-row: 2;

        main {
            padding: 2em 1em 1em 1em;

            section {
                &-titles {
                    font-size: 150%;
                    font-weight: bold;
                    font-style: normal;
                    padding: 0em;
                }

                &-contents {
                    padding: 1em;
                }
            }
        }
    }
}
</style>
