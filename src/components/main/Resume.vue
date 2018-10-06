<template>
  <section id="section-resume">
    <h2 class="section-titles">職務経歴(日時降順)</h2>
    <div class="section-contents">
      <table>
        <thead>
          <th>年月</th>
          <th>企業名</th>
        </thead>
        <tbody>
          <tr><td>2015/5</td><td>株式会社インフィニットループ</td></tr>
          <tr><td>2015/3</td><td>センティリオン株式会社</td></tr>
          <tr><td>2014/11</td><td>USSRエンタープライズ株式会社</td></tr>
          <tr><td>2011/1</td><td>株式会社G.Future.Vision</td></tr>
          <tr><td>2009/4</td><td>株式会社第一コンピュータサービス</td></tr>
        </tbody>
      </table>
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
        #section-resume {
            table {
                margin: 1em;
                border-spacing: 1em;
            }
        }
    }
}
</style>
