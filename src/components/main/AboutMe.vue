<template>
  <section id="section-about-me">
    <a name="about-me"></a>
    <h2 class="section-titles">T. Matsudateについて</h2>
    <div class="section-contents">
      <ul id="about-me">
        <li id="full-name"><p>Tsuyoshi Matsudate</p></li>
        <li id="last-job"><p>株式会社インフィニットループ(Web Developer(at 2015))</p>
          <ul>
            <li id="last-environment">
              <ul class="items">
                <li>PHP(maybe 5.x)</li>
                <li>CakePHP (&lt;2.6)</li>
                <li>Bootstrap</li>
                <li>jQuery</li>
                <li>Windows 8 + Vagrant</li>
              </ul>
            </li>
            <li id="last-product">
              <ul class="items">
                <li id="product-name">Kamimage(カミメージ)</li>
                <li id="product-description">アンケート等の入力フォームを紙媒体の感触を可能な限り再現した上で提供します。</li>
                <li id="product-url">URL: <a href="https://www.kamimage.com">www.kamimage.com</a></li>
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
    name: 'AboutMe'
}
</script>

<style lang="less">
#grids {
    #main {
        main {
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

            #section-about-me {
                #about-me {
                    list-style: none;
                    margin: 1em;

                    ul {
                        list-style: none;
                    }

                    p {
                        padding: 1em;
                        font-size: 120%;
                        font-weight: bold;
                        font-style: normal;
                    }

                    #full-name::before {
                        display: block;
                        content: "氏名";
                    }

                    #last-job::before {
                        display: block;
                        content: "最終職歴";
                    }

                    #last-job {
                        #last-environment::before {
                            display: block;
                            content: "開発環境";
                        }

                        #last-product::before {
                            display: block;
                            content: "担当した製品";
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
