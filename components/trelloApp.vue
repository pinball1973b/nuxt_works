<template>
  <section class="content_section">
    <h2 class="sub_title">{{title.head1}}</h2>
    <h3 class="sub_title_section">{{title.head2}}</h3>
    <div class="article_box">
      <article class="trello_card" v-for="trello in trellos">
          <h4><a :href="trello.shortUrl">{{trello.name}}</a></h4>
          <div class="inner">
            <div class="label">
              <label class="card_btn_input" :for="'card_'+trello.id">
                <span class="label_box" :class="'id_'+trello.idList"></span>
              </label>
            </div>
            <input class="card_chk" type="checkbox" :id="'card_'+trello.id">
            <div class="display-none">
              <div class="desc">
                <div class="desc_inner">
                  <h5><a :href="trello.shortUrl">{{trello.name}}</a></h5>
                  <span class="label_box" :class="'id_'+trello.idList"></span>
                  <div class="desc_text">
                    {{trello.desc}}
                  </div>
                  <div class="desc_btn_box">
                    <div class="close_btn">
                      <label class="card_btn_input" :for="'card_'+trello.id">
                        閉じる
                      </label>
                    </div>
                    <div class="trello_link">
                      <a :href="trello.shortUrl">trelloで編集</a>
                    </div>
                  </div>
                </div>
              </div>
              <div class="overlay"></div>
            </div>
          </div>
      </article>
    </div>
  </section>
</template>
