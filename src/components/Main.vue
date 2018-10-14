<template>
  <div id="main">
    <main>
      <article>
        <AboutMe />
        <Resume />
        <Portfolio />
        <Goals />
        <section id="section-progresses">
          <h2 class="section-titles">開発の進捗状況</h2>
          <div class="section-contents">
            <ul id="progresses">
              <li><strong class="captions">Sheave</strong>
                <p class="descriptions">Rustで開発しているRTMPサーバです。現在はRed5の完全なクローンにすることを目指しています。</p>
                <p class="badges">Just Started.</p>
              </li>
              <li><strong class="captions">ライブ配信サービス(名称未定)</strong>
                <p class="descriptions">裏で開発する映像配信サービスです。VPSという限られた環境からでも安定して使えるよう、ロードバランサとの親和性を高めることを念頭においています。</p>
                <p class="badges">Just started.</p>
              </li>
              <li><strong class="captions">自作OS(名称未定)</strong>
                <p class="descriptions">ライブストリーミングサーバの負荷を減らすため、受信したパケットにあるメディアデータをスムーズにGPUやその他のハードウェアエンコーダに流せる仕様を考えています。</p>
                <p class="badges">Not yet.</p>
              </li>
              <li><strong class="captions">ChromiumへのGPUビデオでコードの実装(Linux向け)</strong>
                <p class="descriptions">何故かまだGPUデコード機能が実装されていないLinux用のChromiumにその機能を実装します。</p>
                <p class="badges">Not yet.</p>
              </li>
            </ul>
          </div>
        </section>
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

export default {
    name: 'Main',
    components: {
        AboutMe,
        Resume,
        Portfolio,
        Goals
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

            #section-progresses {
                #progresses {
                    list-style: none;
                    margin: 1em;

                    .captions {
                        font-weight: bold;
                    }

                    .descriptions {
                        padding: 1em;
                    }

                    .badges {
                        padding: 1em;
                    }
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
