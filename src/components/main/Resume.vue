<template>
  <section id="section-resume">
    <a name="resume"></a>
    <h2 class="section-titles">職務経歴(日時降順)</h2>
    <div class="section-contents">
      <ul id="resume">
        <li>
          <ul>
            <li class="terms"><p>2015/5 - 2015/7</p></li>
            <li class="companies"><p>株式会社インフィニットループ</p></li>
            <li class="environments">
              <ul class="items">
                <li>PHP (maybe 5.x)</li>
                <li>CakePHP (&lt; 2.6)</li>
                <li>Bootstrap</li>
                <li>jQuery</li>
                <li>Windows 8 + Vagrant</li>
              </ul>
            </li>
            <li class="teams">
              <ul class="items">
                <li>3人</li>
                <li>リーダー1人</li>
                <li>開発担当2人</li>
              </ul>
            </li>
            <li class="works">
              <ul class="items">
                <li>画面の装飾・遷移の追加と修正</li>
                <li>雑用</li>
              </ul>
            </li>
          </ul>
        </li>
        <li>
          <ul>
            <li class="terms"><p>2015/3 - 2015/4</p></li>
            <li class="companies"><p>センティリオン株式会社</p></li>
            <li class="environments">
              <ul class="items">
                <li>Scala</li>
                <li>Play</li>
                <li>Slick</li>
                <li>Linux(Arch)</li>
              </ul>
            </li>
            <li class="teams">
              <ul class="items">
                <li>3人</li>
                <li>リーダー1人</li>
                <li>開発担当2人</li>
              </ul>
            </li>
            <li class="works">
              <ul class="items">
                <li>フルリプレースに際したツール選定(打ち合わせ)</li>
                <li>段階的なリプレース作業(.NET-&gt;Scala)</li>
              </ul>
            </li>
          </ul>
        </li>
        <li>
          <ul>
            <li class="terms"><p>2014/11 - 2015/3</p></li>
            <li class="companies"><p>USSRエンタープライズ株式会社</p></li>
            <li class="environments">
              <ul class="items">
                <li>PHP (maybe 5.x)</li>
                <li>CakePHP (&lt; 2.6)</li>
                <li>Bootstrap</li>
                <li>jQuery</li>
                <li>Linux(Arch)</li>
                <li>Gitolite</li>
              </ul>
            </li>
            <li class="teams">
              <ul class="items">
                <li>3人</li>
                <li>リーダー1人</li>
                <li>開発担当3人(リーダー含む)</li>
              </ul>
            </li>
            <li class="works">
              <ul class="items">
                <li>マニュアル作成</li>
                <li>画面改修</li>
              </ul>
            </li>
          </ul>
        </li>
        <li>
          <ul>
            <li class="terms"><p>2011/1 - 2011/4</p></li>
            <li class="companies"><p>株式会社G.Future.Vision</p></li>
            <li class="environments">
              <ul class="items">
                <li>Python (2.6)</li>
                <li>Django (&lt; 1.0)</li>
                <li>HTML5(canvas)</li>
                <li>CSS3</li>
                <li>Windows Vista</li>
              </ul>
            </li>
            <li class="teams">
              <ul class="items">
                <li>5人</li>
                <li>リーダー1人</li>
                <li>開発担当5人(リーダー含む)</li>
              </ul>
            </li>
            <li class="works">
              <ul class="items">
                <li>Androidアプリの実装方法の調査</li>
                <li>画像処理プログラムの調査</li>
                <li>既存サーバサイドコードの改修</li>
                <li>サーバサイドAPIのモックの作成</li>
              </ul>
            </li>
          </ul>
        </li>
        <li>
          <ul>
            <li class="terms"><p>2009/4 - 2010/4</p></li>
            <li class="companies"><p>株式会社第一コンピュータサービス</p></li>
            <li class="environments">
              <ul class="items">
                <li>Windows XP</li>
                <li>カーナビ実機 + シミュレータ</li>
              </ul>
            </li>
            <li class="teams">
              <ul class="items">
                <li>4人</li>
                <li>リーダー1人</li>
                <li>開発担当4人(リーダー含む)</li>
              </ul>
            </li>
            <li class="works">
              <ul class="items">
                <li>画面上に表示される地図や文言の不備の確認と修正(英語、ドイツ語、ロシア語等)</li>
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
    name: 'Resume'
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

            #section-resume {
                #resume {
                    display: grid;
                    list-style: none;
                    grid-template-rows: repeat(5, auto);

                    & > li {
                        margin: 0em -1em 0em -1em;
                    }

                    & > li:nth-child(odd) {
                        background-color: hsl(90,80%,40%);
                        color: hsl(0,100%,100%);
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

                    .terms {
                        &::before {
                            display: block;
                            content: "勤務期間";
                        }
                    }

                    .companies {
                        &::before {
                            display: block;
                            content: "企業名";
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

                    .teams {
                        &::before {
                            display: block;
                            content: "作業人数";
                        }

                        .items {
                            list-style: outside;
                            margin: 1em 2em 1em 2em;
                        }
                    }

                    .works {
                        &::before {
                            display: block;
                            content: "作業内容";
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
