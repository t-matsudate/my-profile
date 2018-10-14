<template>
  <section id="section-portfolio">
    <h2 class="section-titles">制作実績</h2>
    <div class="section-contents">
      <ul id="products">
        <li>
          <ul>
            <li class="product-name"><p>このページ！</p></li>
            <li class="environments">
              <ul class="items">
                <li>HTML5</li>
                <li>Vue.js</li>
                <li>Less</li>
                <li>CSS Grids</li>
                <li>Nodejs</li>
                <li><strong>Zenfone5z(Android 8.0)</strong> with Termux + Vim + Lighttpd</li>
              </ul>
            </li>
            <li class="points">
              <ul class="items">
                <li>Vue.js, CSS Preprocesser, CSS Gridsに初挑戦しました。</li>
                <li>HTML部分はいつまでも生のままは効率が悪すぎるので、次期バージョン（？）ではJadeかそのあたりに置き換える可能性があります。</li>
                <li>何かご要望があれば装飾を追加します(優先度は低いです)</li>
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

                    .product-name {
                        &::before {
                            display: block;
                            content: "製品名";
                        }
                    }

                    .environments {
                        &::before {
                            display: block;
                            content: "開発環境";
                        }

                        .items {
                            list-style: outside;
                            margin: 1em 2em 1em 2em;
                        }
                    }

                    .points {
                        &::before {
                            display: block;
                            content: "工夫とチャレンジ";
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
}
</style>
