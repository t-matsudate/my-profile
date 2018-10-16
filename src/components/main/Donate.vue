<template>
  <section id="section-donate">
    <h2 class="section-titles">寄付等について</h2>
    <div class="section-contents">
      <p id="paypal-me"><a href="https://www.paypal.me/funchs">Paypal.Me</a></p>
      <p id="donate">現在、Paypal Meによる寄付金を募っております。総額に応じて以下の用途を検討しております。</p>
      <ul id="plans">
        <li>
          <ul>
            <li class="totals"><p>10000円未満</p></li>
            <li class="descriptions">
              <ul class="items">
                <li>食費へ充当</li>
              </ul>
            </li>
          </ul>
        </li>
        <li>
          <ul>
            <li class="totals"><p>10000円以上30000円未満</p></li>
            <li class="descriptions">
              <ul class="items">
                <li>首都圏方面へ面接に向かう際の交通費</li>
                <li>Circle CIとの有料プランの契約</li>
              </ul>
              <p class="notes">札幌に住んでいる都合上、冬季に限っては暖房費に消費していく可能性があります。</p>
            </li>
          </ul>
        </li>
        <li>
          <ul>
            <li class="totals"><p>30000円以上80000円未満</p></li>
            <li class="descriptions">
              <ul class="items">
                <li>デバッグ兼運用テストのためのConoHa VPSとの契約</li>
              </ul>
              <p class="notes">総額から消費できる範囲で最短1年の契約を検討しています。</p>
            </li>
          </ul>
        </li>
        <li>
          <ul>
            <li class="totals"><p>80000円以上</p></li>
            <li class="descriptions">
              <ul class="items">
                <li>未定</li>
              </ul>
              <p class="notes">札幌市内での勉強会の主催等を検討しています。</p>
            </li>
          </ul>
        </li>
        <li>
          <ul>
            <li class="totals"><p>300000円(ゴールその1)</p></li>
            <li class="descriptions">
              <ul class="items">
                <li>デスクトップPCの新調</li>
              </ul>
              <p class="notes">夏頃から完全に壊れちゃいました XD(2018年現在)</p>
            </li>
          </ul>
        </li>
      </ul>
      <p id="note-campfire">サービスの稼働を開始した段階でCamp-fireによる出資の募集に切り替えます。</p>
    </div>
  </section>
</template>

<script>
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

            #section-donate {
                #paypal-me {
                    padding: 1em;
                }

                #donate {
                    padding: 1em;
                }

                #plans {
                    display: grid;
                    grid-template-rows: repeat(5, auto);
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

                    .totals {
                        &::before {
                            display: block;
                            content: "総額";
                        }
                    }

                    .descriptions {
                        &::before {
                            display: block;
                            content: "用途";
                        }

                        .items {
                            list-style: outside;
                            margin: 1em 2em 1em 2em;
                        }
                    }

                    .notes {
                        font-size: 0.8em;
                        font-weight: normal;
                        font-style: normal;
                    }
                }

                #note-campfire {
                    margin: 1em;
                    padding: 1em;
                    background-color: hsl(45,100%,60%);
                    border-radius: 20px;
                }
            }
        }
    }
}
</style>
