<template>
  <section class="container content_page">
    <headerApp></headerApp>
    <div class="app_container">
      <div class="sidebar">
        <sidebarApp></sidebarApp>
      </div>
      <div class="main_content">
        <section class="content_section">
          <div v-if="blockquote">
            <h2 class="sub_title">{{title.head1}}</h2>
            <blockquote>
              <p>Nuxt.js とはユニバーサルな Vue.js アプリケーションを構築するためのフレームワークです。</p>

              <p>クライアントサイド用のディストリビューションと、サーバーサイド用のディストリビューションとを分離して生成している間に行う UI レンダリング に焦点を当てています。</p>

              <p>私たちのゴールは、あるプロジェクトの基礎として利用したり、あるいは既に進行中の Node.js ベースのプロジェクトに追加できる、柔軟なフレームワークを作成することです。</p>

              <p>Nuxt.js は サーバーサイドレンダリング する Vue.js アプリケーションの開発をもっと楽しくするために必要な設定を、あらかじめセットしています。</p>

              <p>それに加えて nuxt generate と呼ばれる別の開発オプションも提供します。これは 静的に生成された Vue.js アプリケーションを構築するためのものです。私たちはこのオプションが、マイクロサービスでウェブアプリケーションを開発するための次の大きな一歩になり得ると信じています。</p>

              <p>Nuxt.js はフレームワークとして、クライアントサイドとサーバーサイド間にまたがる開発を手助けする、たくさんの機能を備えています。例えば、非同期でのデータのやり取りや、Nuxt.js をミドルウェアとして利用することや、レイアウト機能などです。</p>
              <p><a href="https://ja.nuxtjs.org/guide">Nuxt.js とは何か？</a></p>
            </blockquote>
            <div @click="description_open" class="btn orange_btn">
              簡単に言うと
            </div>
          </div>
          <div class="description" v-if="description">
            <h2 class="sub_title">{{title.head2}}</h2>
            <p><img src="~/assets/image/vwb.png"></p>
            <ul>
              <li>レンダリングやルーティングををNuxtが行うため、RailsやPHPはバックエンドに専念できる→フロント・バックの疎結合化</li>
              <li>SSR以外にもSPA、静的ページ生成もできる。</li>
              <li>Vuexを利用したコンポーネント化</li>
              <li>Vue-Routerを利用したルーティング</li>
              <li>サーバサイドレンダリング</li>
              <li>Vue-Metaを利用したSEO対策</li>
            </ul>
            <div class="floder_img">
              <h2 class="sub_title">{{title.head3}}</h2>
              <div class="floder_img_box">
                <div class="image">
                  <img src="~/assets/image/folder.png">
                </div>
                <div class="folder-list">
                  <dl>
                    <dt>assets</dt>
                    <dd>画像・Sass・JavaScriptなど、コンパイルされていないファイルを入れる</dd>
                    <dt>components</dt>
                    <dd>vueのコンポーネントを入れる（拡張子はvue）</dd>
                    <dt>layouts</dt>
                    <dd>レイアウトファイルを入れる</dd>
                    <dt>middleware</dt>
                    <dd>アプリケーションのミドルウェアを入れる。（今回は使っていない）</dd>
                    <dt>page</dt>
                    <dd>ページ用のvueファイルを入れる。例：example.com/indexの場合、index.vue</dd>
                    <dt>plugins</dt>
                    <dd>ルートの Vue.js アプリケーションをインスタンス化する前に実行したい JavaScript プラグインを入れる。</dd>
                    <dt>static</dt>
                    <dd>コンパイルしない静的ファイルを入れる。</dd>
                    <dt>store</dt>
                    <dd>Vueストアを入れる。JavaScriptでかかれる。</dd>
                  </dl>
                </div>
              </div>
            </div>
          </div>
        </section>
      </div>
    </div>
  </section>
</template>
<script>
import headerApp from '~/components/headerApp.vue'
import contentApp from '~/components/contentApp.vue'
import sidebarApp from '~/components/sidebarApp.vue'
export default {
  components: {
    headerApp,
    contentApp,
    sidebarApp
  },
  head: {
    link: [
      { rel: 'stylesheet', href: '//maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css' }
    ]
  },
  data: function () {
    return {
      description: false,
      blockquote: true,
      title: {
        head1: 'Nuxt.jsとは',
        head2: 'Vue.js + Webpack + BabelでRailsやPHPフレームワークのフロント部分を代わりにやってくれるイメージ。',
        head3: 'ディレクトリ構成はこんな感じ'
      }
    }
  },
  methods: {
    description_open: function () {
      this.description = true
      this.blockquote = false
    }
  }
}
</script>

<style lang="scss">
.floder_img_box {
  display: flex;
  .image {
    width: 20%;
    img {
      width: 100%;
    }
  }
  .folder-list {
    margin-left: 20px;
    dd {
      margin-bottom: 10px;
    }
  }
}

.opacity_05 {
  opacity: 0.5;
}

.width80 {
  width: 80%;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}

.orange_btn {
  background: #ffa500;
  padding: 10px;
  border-radius: 4px;
  color: #fff;
  font-weight: bold;
  width: 100%;
  font-size: 1.4rem;
  &:hover {
    color: #fff;
  }
}
</style>
