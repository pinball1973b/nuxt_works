<template>
  <div id="contentApp" class="content_container">
    <h2 class="sub_title">{{$store.state.title}}</h2>
    <ul class="agenda_list content_agenda">
      <li v-for="item in $store.state.items"><nuxt-link :to="contentUri(item.uri)">{{item.list}}</nuxt-link></li>
    </ul>
  </div>
</template>
<script>
export default {
  methods: {
    contentUri (uri) {
      return `/${uri}`
    }
  }
}
</script>

<style lang="scss">
.sub_title {
  color: #666;
  border-left: solid 15px #666;
  padding: 0 15px;
}
.sub_title_index {
  color: #666;
  border-bottom: 1px solid #999;
  padding-bottom: 5px;
  margin-bottom: 20px;
}
.agenda_list {
  padding: 0;
  &.content_agenda {
    font-size: 2rem;
    li {
      list-style: none;
      margin-bottom: 10px;
      border-bottom: 1px dotted #aaa;
      padding-bottom: 5px;
      a {
        dislay: block;
      }
    }
  }
}
</style>
