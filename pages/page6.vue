<template>
  <section class="container content_page">
    <headerApp></headerApp>
    <div class="app_container">
      <div class="sidebar">
        <sidebarApp></sidebarApp>
      </div>
      <div class="main_content">
        <section class="content_section">
          <h2 class="sub_title">{{main_title}}</h2>
          <div>
            <article v-for="content in contents" class="article_section">
              <h3>{{content.title}}</h3>
              <p>{{content.text}}</p>
              <p><nuxt-link :to="content.uri">{{content.link_text}}</nuxt-link></p>
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
      main_title: '使い方例',
      contents: [
        {title: 'Wordpressテンプレート', text: 'Wordpressテンプレートして使用する。REST APIを利用。', uri: 'https://nuxtwp.now.sh/', link_text: 'Nuxt WordPress | Home'},
        {title: 'Todoリスト', text: '定番のTodoリストアプリ', uri: 'https://todomvc.nuxtjs.org/', link_text: 'todos'},
        {title: 'Firebaseを使ったSSRブログ', text: 'バックエンドにFirebaseを使ったブログ。', uri: 'https://nuxt-ssr-blog.firebaseapp.com/', link_text: 'Awesome JS SSR Blog'}
      ]
    }
  },
  methods: {

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
