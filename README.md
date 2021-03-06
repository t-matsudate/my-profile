T. Matsudate's Profile to be created by Vue.js
===

これは @t-matsudate が日本国内での就職活動を有利に進めていくために公開するポートフォリオ兼進捗状況の公開用ウェブページです(時々、実験的に何かの動的コンテンツを生成するかもしれません)。主に以下の内容をウェブ化します：

* 簡単な自己紹介
  * 最終職歴
  * 利用中のSNS 等
* 職歴と現状のスキルについて
* ウェブデザイン及び技術的なポートフォリオ
  * まず、このウェブページが完成すれば、これ自体をポートフォリオにできます。
* 当面の目標
  * 技術的に成し遂げたい事
  * 人間的(社会的？)な最終到達点 等
* 進捗状況
  * 私自身の各リポジトリのコミット状況(CIを経由してあればそのバッジを添えます)
  * 就職活動の現在の状況 等
* RTMPサーバ等の実装の記録(ブログ形式？)

### 開発環境

* Termux on Zenfone5Z
* Vue.js & Less
* Vim

#### 端末のスペック

* Snapdragon845(8 cores)
* RAM 6GB
* Storage 128GB

#### 外部機器

* Majestouch Minila AIR(黒軸)

ページ作成の経緯
---

私がこのウェブページを作ろうとすることには、以下の目的があります：

1. 就職活動における不利の原因の解消もしくは緩和
2. 個人事業主としての活動再開に向けての対外的なアピール
3. 流行のフロントエンドツールの試用

### 就職活動において圧倒的に不利

どう加算していっても高々2年の私の職歴は、私自身の現在の年齢を以てアピールするには余りにも弱すぎた様です。その原因は以下にあると考えています：

1. 2年と続かない疎で不連続な経歴の多発
2. 1.が原因である、確かな業務経験及び業務レベルの技術の圧倒的不足
3. 1., 2.が原因で挫折を繰り返すことによる労働意欲や自信の減衰
4. 集団から離れる時間が増えるごとに薄れゆく、所謂「模範的で常識的な人との接し方」の記憶

上記の原因に対して、このウェブページの制作を通して以下の対処を行います：

* ポートフォリオに記載する内容を自力で生成し、就職の裾野を広げる。
* 不足しているウェブフロントエンドの知識・技術や流行のバックエンド技術への理解を深める。
* 上記の対処を行う事により、就職活動における技術的なアピールの材料を増やし、自信の回復に寄与させる。

*4.については別な形で対応を考えます。*

### 個人事業主としての活動再開の準備

これを以て就職活動に繋げても尚だめだった場合に備えて、個人事業主として再び活動していく準備として以下のツール及びサービス開発を再開し、その活動をアピールするものとしても活用していきます：

1. RTMPサーバ
  * 当面はClojureでRed5の機能を拡張しつつ連携させていく実装を行います。(**原則非公開**)
    * プロジェクト自体は[Gitlab](https://gitlab.com)に置きます。
  * 最終的には完全なRust製にするつもりです。
    * Rust実装は、公開可能な部分については(可能な限り)毎日21:00あたりから以下のいずれかのサービスでライブ配信を行う予定です：
      * [YouTube](https://youtube.com/tmatsudate/live)
    * Flashの存在が大前提になっているAPIを完全にHTML5ベースに置き換えていきます。
    * WebAssemblyでフロントエンド側と連携を取れるようにするのが理想です。
    * 最終的にはRTMP部分を取り除き、HTTP Live Streamingで送受信されるデータだけで映像をサービスできるようにしたいと思います。
2. 映像配信サービス本体
   * 当面はClojure製にします。
     * 出力するするHTMLを表現しやすいです([hiccup](https://github.com/weavejester/hiccup)があればVector構造に収まったキーワードとマップをコンパイルするだけでHTMLを生成できます)。
     * ビルドツール[Leiningen](https://github.com/technomancy/leiningen)が使いやすく、また覚えやすいです。
     * サーバサイドと同様の構文で変換できるJavascriptトランスパイラ([Clojurescript](https://clojurescript.org))があります。  
     * S式だからコードを書く上であまり多くの事を同時に覚えなくていいのは大きいです！*
     * 何よりここ数年で一番私の手に馴染んでいます。
   * Clojureで拡張したRed5サーバとの迅速かつ柔軟な連携を可能にします。
     * Red5もまたJava製であるため親和性は高いと考えます(詳細は当該リポジトリのREADMEやドキュメントに記載します)。
   * .NET Runtime版のバイナリ([Clojure CLR](https://clojure.org/about/clojureclr))もあります。
     * Java側に何か都合の悪い事が起こっても、ランタイムの切り替えにそう多くの時間を必要としないでしょう。
     * Clojureのコードのまま、[Blazor](https://github.com/aspnet/Blazor)でサーバの各部分を再実装する事も十分に可能です。
3. [Unix v6](https://github.com/mit-pdos/xv6-public)をベースにしたUnix系OSの実装
   * 目下構想中のサーバ用OS実装の足掛かりにしたいと思います。
4. 映像視聴におけるブラウザ間の差異の撲滅もしくは緩和
   * GPUビデオデコードを全OSの全ブラウザに対応させたいです。
   * HTTP Live Streamingをすべてのブラウザにおいてネイティブ対応させたいですし、当該ストリーミング技術用のネットワーク通信プロトコルを新たに策定してみたいとも思います。
   * WebRTCについても同様です。
   * ただし、IE/Edge/SafariはOSに固くバンドルされており別途環境を揃える必要があることから、対応は後手に回ると思います…。

RTMPサーバ及び配信サービスについては、いずれにしてもバックエンド・フロントエンド共に最終的にはRust製にするつもりで開発していきます。Rustで実装しきれなさそうな場合はKotlinの採用を検討しています。その理由は単純です：

**Red5が乗っかっているSpring FrameworkがKotlinを使い始めているため**(できるだけモダンとされている言語を使いたく、それでいてフレームワーク側とこちら側とで言語の種類を揃えたい。同時に使う道具の数をあまり増やしたくないといったことです)。

#### 個人事業を完全に諦める、もしくは他の仕事が先に見つかった時

その場合は、営利目的でのサービスの公開を中止/中断し、就職活動/日常業務に集中します。しかし、ツールや関連ライブラリの開発は公開可能な範囲で続行します。

ウェブページの実装状況
---

* [x] 大枠のレイアウト(Grid)の決定
* [x] ヘッダのデザイン
* [x] メニューのデザイン及びコンテンツへのリンク
* [x] プロフィール
* [x] 職歴
* [x] ポートフォリオ
* [x] 目標
* [x] 開発の進捗状況
* [x] 寄付等について
* [ ] 実装の記録(WIP)

ライセンス
---

未定

&copy; 2018-2019 t-matsudate
