<template>
  <section class="container content_page">
    <headerApp></headerApp>
    <div class="app_container">
      <div class="sidebar">
        <sidebarApp></sidebarApp>
      </div>
      <div class="main_content">
        <section class="content_section">
          <div>
            <h2 class="sub_title">{{title.head1}}</h2>
            <p>※Node.jsやnpmが予めインストールされていることが前提です。</p>
            <article class="article_section">
              <h3>{{title.head2}}</h3>
              <code>npm install -g vue-cli</code>
            </article>
            <article class="article_section">
              <h3>{{title.head3}}</h3>
              <code>$ vue init nuxt-community/starter-template &lt;project-name&gt;</code>
              <p>依存するパッケージをインストール</p>
              <code>
                $ cd &lt;project-name&gt;
                $ npm install
              </code>
              <p>プロジェクトを起動</p>
              <code>$ npm run dev</code>
              <p>http://localhost:3000でコードが動いている。</p>
            </article>
            <article class="article_section">
              <h3>{{title.head4}}</h3>
              <p>GitHubよりcloneして<code>$ npm run dev</code>で起動して下さい。</p>
              <p>※localhost8080で起動します</p>
              <p>※詳しくは<a href="https://ja.nuxtjs.org/">公式ドキュメント</a>を読んで下さい。</p>
            </article>
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
      title: {
        head1: 'Nuxt.jsのはじめ方',
        head2: 'vue-cliをインストール',
        head3: 'Nuxtスターターテンプレートをインストール',
        head4: 'この勉強会資料',
        head5: ''
      }
    }
  },
  methods: {

  }
}
</script>

<style lang="scss">
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
