<template>
  <section id="section-portfolio">
    <a name="portfolio"></a>
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
        <li>
          <ul>
            <li class="product-name"><p><a href="https://t-matsudate.github.io/rtmp-reports/">RTMP Implementation Reports</a><br>RTMP サーバの実装メモと直近の仕様の整理</p></li>
            <li class="environments">
              <ul class="items">
                <li>Zenfone 5Z (Android 9)</li>
                <li>Termux</li>
                <li>Vim</li>
                <li>Vue.js 2.6.10</li>
                <li>Vue Router 3.0.7</li>
                <li>Markdown-it 9.1.0 with its many plugins.</li>
                <li>Katex 0.11.0</li>
                <li>Highlight.js 9.15.10</li>
                <li>Flowchart.js 1.12.2</li>
                <li>GitHub Markdown CSS(<a href="https://www.npmjs.com/package/github-markdown-css">NPM</a>)</li>
                <li>Less 3.10.3</li>
              </ul>
            </li>
            <li class="points">
              <ul class="items">
                <li>個別の記事にアクセスできるようにルーティングしてみました。</li>
                <li>しかし、GitHubが抱えているサーバサイドのルーティング機能との相性があまりよくなく、<strong>ロケーションバーからの直接の移動ができない</strong>状況です。<br>(npm run serveで動かした時は素で移動できてたのになあ…)</li>
                <li>よって、記事が一通り出揃った頃合いでNuxt.jsによる静的サイト生成に切り替えます。</li>
                <li>記事自体はMarkdown-itにプラグインを色々追加して記法やマークアップのパターンを拡張して表現力を高めています。<br>(詳しくはソースのpackage.jsonをご覧ください)</li>
                <li><em>(NPMってJSのファイル容量が250KBを超えると警告してくるんだね…)</em></li>
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
                        background-color: hsl(90,80%,40%);
                        color: hsl(0,100%,100%);

                        a {
                            color: hsl(0,100%,100%);
                        }
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
