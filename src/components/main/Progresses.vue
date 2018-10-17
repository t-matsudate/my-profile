<template>
  <section id="section-progresses">
    <a name="progresses"></a>
    <h2 class="section-titles">開発の進捗状況</h2>
    <div class="section-contents">
      <ul id="progresses">
        <li>
          <ul id="sheave">
            <li class="product-names"><p>Sheave</p></li>
            <li class="descriptions"><p>Rustで開発しているRTMPサーバです。現在はRed5の完全なクローンにすることを目指しています。</p></li>
          </ul>
        </li>
        <li>
          <ul id="service">
            <li class="product-names"><p>ライブ配信サービス(名称未定)</p></li>
            <li class="descriptions"><p>裏で開発する映像配信サービスです。VPSという限られた環境からでも安定して使えるよう、ロードバランサとの親和性を高めることを念頭においています。</p></li>
          </ul>
        </li>
        <li>
          <ul id="os">
            <li class="product-names"><p>自作OS(名称未定)</p></li>
            <li class="descriptions"><p>ライブストリーミングサーバの負荷を減らすため、受信したパケットにあるメディアデータをスムーズにGPUやその他のハードウェアエンコーダに流せる仕様を考えています。</p></li>
          </ul>
        </li>
        <li>
          <ul id="gpu">
            <li class="product-names"><p>ChromiumへのGPUビデオデコードの実装(Linux向け)</p></li>
            <li class="descriptions"><p>何故かまだGPUデコード機能が実装されていないLinux用のChromiumにその機能を実装します。</p></li>
          </ul>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
    name: 'Progresses'
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

            #section-progresses {
                #progresses {
                    display: grid;
                    list-style: none;
                    grid-template-rows: repeat(4, auto);

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

                    #sheave {
                        &::after {
                            display: block;
                            content: url("https://circleci.com/gh/t-matsudate/sheave.svg?style=svg");
                        }
                    }

                    #service {
                        &::after {
                            display: block;
/*                            content: url("https://circleci.com/gh/t-matsudate/hoge.svg?style=svg");
*/
                        }
                    }

                    #os {
                        &::after {
                            display: block;
/*                            content: url("https://circleci.com/gh/t-matsudate/fuga.svg?style=svg");
*/
                        }
                    }

                    #gpu {
                        &::after {
                            display: block;
/*                            content: url("https://circleci.com/gh/t-matsudate/piyo.svg?style=svg");
*/
                        }
                    }

                    .product-names {
                        &::before {
                            display: block;
                            content: "製品名";
                        }
                    }

                    .descriptions {
                        &::before {
                            display: block;
                            content: "概要";
                        }
                    }
                }
            }
        }
    }
}
</style>
