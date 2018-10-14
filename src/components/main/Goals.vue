<template>
  <section id="section-goals">
    <h2 class="section-titles">到達目標</h2>
    <div class="section-contents">
      <ol id="goals">
        <li>
          <ul>
            <li class="declarations"><p>映像視聴におけるブラウザ間の差異の緩和</p></li>
            <li class="descriptions">
              <p>ライブ映像視聴における、ブラウザ・OS間の違いやズレを0に近づけていきます。</p>
              <p><i class="fab fa-firefox"></i>
              == <i class="fab fa-chrome"></i>
              == <i class="fab fa-edge"></i><small>(Maybe)</small>
              == <i class="fab fa-safari"></i><small>(Maybe)</small>
              </p>
            </li>
            <li class="concretes">
              <ul class="items">
                <li>HTTP Live Streamingのネイティブ実装をFirefoxとChromeにも持ってきます(どちらもデスクトップ版)。</li>
                <li>GPU Video DecoderをLinuxのChromiumにも持ってきます。</li>
                <li>WebRTCのネイティブ実装をFirefoxにも持ってきます。</li>
                <li><small>(金銭的余裕と環境があれば、EdgeとSafariにも同様の対応を行います。)</small></li>
                <li>新ProtocolであるSRTのネイティブ実装をすべてのブラウザに持ってきます(まずはFirefoxとChromeから)。</li>
              </ul>
            </li>
          </ul>
        </li>
        <li>
          <ul>
            <li class="declarations"><p>HTTP Live Streamingのサーバ&amp;ブラウザ向けプロトコル(URLスキーム)化</p></li>
            <li class="descriptions"><p>1.の実装を容易にするために、HLS(HTTP Live Streaming)で通信するためのプロトコルのRFCをIETFに提出します。</p></li>
            <li class="concretes">
              <ul class="items">
                <li>IETFに対するRFCの書き方を学びます。</li>
                <li>プロトコル制定に必要なパケットの設計の仕方と安全で効率的な通信の方法を調査します。</li>
                <li>当該プロトコルのサンプル実装を少しずつGitHub等にて公開していきます。</li>
                <li>各種ブラウザの標準実装に向けてコミットしていきます。</li>
              </ul>
            </li>
          </ul>
        </li>
        <li>
          <ul>
            <li class="declarations"><p>映像配信に特化したLinux/UnixベースOSの開発</p></li>
            <li class="descriptions">
              <p>これは私自身のスキルアップのための挑戦でもあります。時期については未定ですが、非WindowsなサーバであってもGPUやエンコーダチップとサーバプログラムとの接続をより容易に実現できる商用OSを開発していきます。</p>
            </li>
            <li class="concretes">
              <ul class="items">
                <li>配信リクエストの1つ1つをデバイスファイルで受け持ち、それらとハードウェアビデオエンコーダとを接続させ、時間的ズレを限界まで抑えた処理を実現します。</li>
                <li>ライブ配信用の映像ファイルの保管に適したファイルシステムを設計します。</li>
                <li>最初はRustを使ってUnix v6を小さく実装していきます。</li>
                <li>Unixの仕組みが分かってき来たら、徐々にLinuxベースに切り替えていきます(多分ArchベースもしくはGentooベースになります)。</li>
                <li>すべての実装が完了次第、弊事業の実運用サーバマシンを購入し、インストールして実践します(その時はCamp-fireで出資金を募ります)。</li>
                <li>実運用でも安定していることを確認でき次第、商品化します。</li>
              </ul>
            </li>
          </ul>
        </li>
        <li>
          <ul>
            <li class="declarations"><p>北海道内で月収60万超を稼げる事業を成立させ、悠々自適な生活を送る</p></li>
            <li class="descriptions">
              <p>自分が気に入った部屋の中で冷暖房の恩恵を受けながら開発していたいと思いませんか？私はそれを今後30 - 40年の間で実現するつもりです。</p>
            </li>
            <li class="concretes">
              <ul class="items">
                <li>まずは札幌市内で月収60万スタートできる状態を自力で作ります。その為に、</li>
                <li>完成した映像配信サービスの個人ユーザを着実に増やし、そのサービスが安定してきたことを確認次第、企業やコミュニティ向けにもサービスを展開し、</li>
                <li>個人向けの純粋な営業利益、企業向けのサービス単価、そしてクラウドファンディングでの出資金等々、あらゆる方面から資金を獲得していき、</li>
                <li>自分自身で勉強会等を主催したり登壇したりするついでに弊サービスでストリーミングしていくことで、より広い層へのアピールを着実に実施し多目的での配信サービスの新スタンダードを目指していきます(少なくとも、日本国内において)。</li>
                <li>それらを着々と積み重ねていくことで、新築のマンションを買えるところまで財力を向上させます(しかし目指すのは<strong>億</strong>ションです)。</li>
                <li>そして、皆で一緒にぬくぬくしましょう！</li>
                <li><small>(他にも考えていることはありますが、ひとまずここまで)</small></li>
              </ul>
            </li>
          </ul>
        </li>
      </ol>
    </div>
  </section>
</template>

<script>
export default {
    name: 'Goals'
}
</script>

<style lang="less">
#grids {
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

        #section-goals {
            #goals {
                display: grid;
                grid-template-rows: auto;
                list-style: none;
                counter-reset: declarations;

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
 
                .fab {
                    font-size: 300%;
                }

                .fa-firefox {
                    color: hsl(20,100%,60%);
                }

                .fa-chrome {
                    color: hsl(90,100%,60%);
                }

                .fa-edge {
                    color: hsl(225,100%,60%);
                }

                .fa-safari {
                    color: hsl(200,100%,40%);
                }

                .declarations {
                    &::before {
                        display: block;
                        list-style: outside;
                        counter-increment: declarations;
                        content: "目標" counter(declarations);
                    }
                }

                .descriptions {
                    &::before {
                        display: block;
                        content: "概要";
                    }
                }

                .concretes {
                    &::before {
                        display: block;
                        content: "実行計画";
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
