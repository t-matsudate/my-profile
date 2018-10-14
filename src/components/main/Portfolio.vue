<template>
  <section id="section-portfolio">
    <h2 class="section-titles">制作実績</h2>
    <div class="section-contents">
      <ul id="products">
        <li><p>このページ！</p>
          <ul>
            <li class="environments">
              <ul class="items">
                <li>Vue.js</li>
                <li>Less</li>
                <li>(後々で生HTMLをJadeに置き換えるかも)</li>
              </ul>
            </li>
          </ul>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
    name: 'Portfolio'
}
</script>

<style lang="less">
#grids {
    #main {
        main {
            padding: 1em;

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

            #section-portfolio {
                #products {
                    display: grid;
                    grid-template-rows: auto;
                    list-style: none;

                    & > li {
                        margin: 0em -1em 0em -1em;
                    }

                    & > li:nth-child(odd) {
                        background-color: rgb(0,0,0);
                        color: rgb(255,255,255);
                    }

                    ul {
                        list-style: none;
                        margin: 1em 2em 1em 2em;
                    }

                    p {
                        padding: 1em;
                        font-size: 120%;
                        font-weight: bold;
                        font-style: normal;
                    }

                    .environments::before {
                        display: block;
                        content: "開発環境";
                    }

                    .items {
                        list-style: outside;
                        margin: 1em 2em 1em 2em;
                    }
                }
            }
        }
    }
}
</style>
