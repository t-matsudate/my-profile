<template>
  <div id="main">
    <main>
      <article>
        <AboutMe />
        <Resume />
        <Portfolio />
        <Goals />
        <Progresses />
        <section id="section-donate">
          <h2 class="section-titles">寄付等について</h2>
          <div class="section-contents">
            <p id="paypal-me"><a href="https://www.paypal.me/funchs">Paypal.Me</a></p>
            <div id="donate">現在、Paypal Meによる寄付金を募っております。総額に応じて以下の用途を検討しております。
              <ul id="plans">
                <li><strong class="captions">10000円未満</strong>
                  <p class="descriptions">食費へ充当します。</p>
                </li>
                <li><strong class="captions">10000円以上30000円未満</strong>
                  <p class="descriptions">
                    首都圏方面へ面接に向かう際の交通費<br>
                    Circle CIとの有料プランの契約
                  </p>
                  <p class="notes">札幌に住んでいる都合上、冬季に限っては暖房費に消費していく可能性があります。</p>
                </li>
                <li><strong class="captions">30000円以上80000円未満</strong>
                  <p class="descriptions">デバッグ兼運用テストのためのConoHa VPSとの契約</p>
                  <p class="notes">総額から消費できる範囲で最短1年の契約を検討しています。</p>
                </li>
                <li><strong class="captions">80000円以上</strong>
                  <p class="descriptions">未定</p>
                  <p class="notes">札幌市内での勉強会の主催等を検討しています。</p>
                </li>
                <li><strong class="captions">300000円(ゴールその1)</strong>
                  <p class="descriptions">デスクトップPCの新調</p>
                  <p class="notes">夏頃から完全に壊れちゃいました XD(2018年現在)</p>
                </li>
              </ul>
              <p>サービスの稼働を開始した段階でCamp-fireによる出資の募集に切り替えます。</p>
            </div>
          </div>
        </section>
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

export default {
    name: 'Main',
    components: {
        AboutMe,
        Resume,
        Portfolio,
        Goals,
        Progresses
    }
}
</script>

<style lang="less">
#grids {
    #main {
        grid-row: 2;
        grid-column: 2;

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

            #section-donate {
              #paypal-me {
                  padding: 1em;
              }

              #donate {
                  padding: 1em;
              }

              #plans {
                  list-style: none;
                  margin: 1em;

                  .captions {
                      font-weight: bold;
                  }

                  .descriptions {
                      padding: 1em;
                  }

                  .notes {
                      padding: 1em;
                  }
              }
            }
        }
    }
}
</style>
