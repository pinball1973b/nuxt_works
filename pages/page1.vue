<template>
  <section class="container content_page">
    <headerApp></headerApp>
    <div class="app_container">
      <div class="sidebar">
        <sidebarApp></sidebarApp>
      </div>
      <div class="main_content">
        <contentApp></contentApp>
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
</style>
