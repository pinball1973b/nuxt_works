<template>
  <section class="container content_page">
    <headerApp></headerApp>
    <div class="app_container">
      <div class="sidebar">
        <sidebarApp></sidebarApp>
      </div>
      <div class="main_content">
        <section class="content_section">
          <h2 class="sub_title">{{title.head1}}</h2>
          <div>
            <article class="article_section">
              <h3>{{title.head2}}</h3>
              <p>components/contentApp.vueにdataを書いてエラー</p>
              <pre>
data :{
  title: 'angenda'
}
              </pre>
              <p>dataはpageに書く。または、storeにstateとして書く。</p>
            </article>
            <article class="article_section">
              <h3>{{title.head3}}</h3>
              <p>pageにdataをそのまま書いてエラー</p>
              <pre>
data: function () {
  return {
    description: false,
    blockquote: true
  }
}
              </pre>
              <p>dataは関数として書く。</p>
            </article>
            <article class="article_section">
              <h3>{{title.head4}}</h3>
              <p>elは書かずに、そのままmethodsを書く。</p>
              <pre>
methods: {
  description_open: function () {
    this.description = true
    this.blockquote = false
  }
}
              </pre>
            </article>
            <article class="article_section">
              <h3>{{title.head5}}</h3>
              <p>function () の後にスペースを入れ忘れてエラー</p>
              <p><img src="~/assets/image/error.png"></p>
            </article>

            <article class="article_section">
              <h3>{{title.head6}}</h3>
              <p>Vueファイル内にCSSを書いているので、もにょもにょする。</p>
              <p>ちゃんと設計しましょう！</p>
            </article>

            <article class="article_section">
              <h3>{{title.head7}}</h3>
              <p>nuxt-linkは内部リンクのみ、外部リンクは通常通りa要素にhrefをbindすること。</p>
            </article>

            <article class="article_section">
              <h3>{{title.head8}}</h3>
              <p>assets内の画像のURLがwebpackによって書き替わるので、dataの中に入れようとすると迷う</p>
            </article>

            <article class="article_section">
              <h3>{{title.head9}}</h3>
              <p>dataの中に未整形のcodeを入れる方法がわからなかったため。そもそも手動でやるもんじゃない。。。</p>
            </article>

            <article class="article_section">
              <h3>{{title.head10}}</h3>
              <p>何をcompornentsにして、なにをstateにして、何をdataにするのか、考慮なしに始めたのでブレる。</p>
              <p>ワイヤーフレームもなしに始めたので、スライドを作るつもりがいつの間にかサイトみたいになっている。</p>
            </article>

          </div>
        </section>
      </div>
    </div>
  </section>
</template>
<script>
import headerApp from '~/components/headerApp.vue'
import sidebarApp from '~/components/sidebarApp.vue'
export default {
  components: {
    headerApp,
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
        head2: 'vue-componentsにdataは書けない',
        head3: 'dataは関数として書く',
        head4: 'インスタンスをcompornentsに書いてエラー',
        head5: 'スペース入れ忘れでESLintに怒られる。',
        head6: 'JavaScript in CSSでぐぬぬ。。。',
        head7: 'nuxt-linkを使い間違える',
        head8: 'assetsのimgの扱い',
        head9: 'この文書自体をdataに入れてv-forにしようとしたけど挫折',
        head10: 'そもそも、設計しないで書き始めたので色々ブレる'
      }
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
