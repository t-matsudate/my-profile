<template>
  <section id="section-about-me">
    <h2 class="section-titles">T. Matsudateについて</h2>
    <div class="section-contents">
      <ul id="about-me">
        <li>氏名: Tsuyoshi Matsudate</li>
        <li>最終職歴: 株式会社インフィニットループ(Web Developer(at 2015))
          <ul id="last-environment">
            <li><strong class="captions">開発環境</strong>
              <ul class="items">
                <li>PHP(maybe 5.x)</li>
                <li>CakePHP (&lt;2.6)</li>
                <li>Bootstrap</li>
                <li>jQuery</li>
                <li>Windows 8 + Vagrant</li>
              </ul>
            </li>
            <li><strong class="captions">担当した製品</strong>
              <ul id="last-product">
                <li>製品名: Kamimage(カミメージ)</li>
                <li>概要: アンケート等の入力フォームを紙媒体の感触を可能な限り再現した上で提供します。</li>
                <li>URL: <a href="https://www.kamimage.com">www.kamimage.com</a></li>
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
                }

                #last-environment {
                    list-style: none;
                    margin: 1em;
                }

                #last-product {
                    list-style: outside;
                    margin: 1em;
                }

                .captions {
                    font-weight: bold;
                }

                .items {
                    list-style: outside;
                    margin: 1em;
                }
            }
        }
    }
}
</style>
