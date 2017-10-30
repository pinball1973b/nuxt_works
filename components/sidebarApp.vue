<template>
  <div id="sidebarApp" class="sidebar_app">
    <ul class="agenda_list sidebar_list">
      <li v-for="item in $store.state.items"><a :href="item.uri">{{item.list}}</a></li>
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
.sidebar_list{
  -webkit-padding-start: 0;
   li {
     list-style: none;
     margin-bottom: 10px;
   }
 }
</style>
