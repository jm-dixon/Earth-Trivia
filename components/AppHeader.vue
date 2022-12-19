<template>
  <div class="Header flex">
    <div class="flex jc-fs">
      <h1>
        <nuxt-link class="Header__titleLink" to="/">
          <b>{{ websiteTitle }}</b>
        </nuxt-link>
      </h1>
    </div>
    <div class="flex jc-fe">
      <nuxt-link to="/quotes" target="_blank">
        <b>Quotes</b>
      </nuxt-link>
      <nuxt-link to="/facts" target="_blank">
        <b>Facts</b>
      </nuxt-link>
      <nuxt-link to="/blog" target="_blank">
        <b>Blog</b>
      </nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AppHeader',
  data () {
    return {
      websiteTitle: 'EarthTrivia'
    }
  }
}
</script>

<style type="text/css">
/* stylelint-disable */
.Header {
  text-align: right;
  width:100%;
  position: absolute;
  z-index: 1;
}
.Header__titleLink {
  padding: 0 !important;
  color: var(--color-neruoscriptBlue) !important;
  font-size: 1em !important;
}
.Header a {
  text-decoration: none;
  font-size: 1.2em;
  color: var(--color-whiteSmoke);
  padding: 1.5em 1.5em 1.5em 1.5em;
  float: right;
  text-shadow: 2px 2px var(--color-black);
}
.Header a:hover {
  color: var(--color-neruoscriptBlue);
}
.Header h1 {
  text-align: left;
  color: var(--color-whiteSmoke);
  padding: 0.3em 0.3em 0.3em 1em;
  margin: 0;
  text-shadow: 2px 2px var(--color-black);
}
.Header > div {
  width: 50%;
}
</style>
