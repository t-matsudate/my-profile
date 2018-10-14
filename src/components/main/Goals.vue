<template>
  <section id="section-goals">
    <h2 class="section-titles">到達目標</h2>
    <div class="section-contents">
      <ul id="goals">
        <li><strong class="captions">映像視聴におけるブラウザ間の差異の緩和</strong>
          <p class="descriptions"><i class="fab fa-firefox"></i><br>
            == <i class="fab fa-chrome"></i><br>
            == <i class="fab fa-edge"></i>(Maybe)<br>
            == <i class="fab fa-safari"></i>(Maybe)
          </p>
        </li>
        <li><strong class="captions">HTTP Live Streamingのプロトコル化</strong>
          <p class="descriptions">Safari以外でもライブストリーミングの環境をより安定したものとするため、HLS(HTTP Live Streaming)をIETFのRFCのテーブルに載せます。</p>
        </li>
        <li><strong class="captions">映像配信に特化したLinux/UnixベースOSの開発</strong>
          <p class="descriptions">これは私自身のスキルアップのための挑戦でもあります。時期については未定ですが、非WindowsなサーバであってもGPUやエンコーダチップとサーバプログラムとの接続をより容易に実現できる商用OSを開発していきます。当面はUnix v6の実装をベースにRustで開発していく予定です。</p>
        </li>
        <li><strong class="captions">北海道内で月収60万超を稼げる事業を成立させ、悠々自適な生活を送る</strong>
          <p class="descriptions">自分が気に入った部屋の中でぬくぬくしながら開発していたい。していたくない？</p></li>
      </ul>
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
                list-style: none;
                margin: 1em;

                .captions {
                    font-weight: bold;
                }

                .descriptions {
                    padding: 1em;
                }
            }
        }
    }
}
</style>
