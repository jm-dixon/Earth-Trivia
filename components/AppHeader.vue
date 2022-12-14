<template>
  <div class="Header flex">
    <div class="flex jc-fs">
      <h1>
        <b>{{ websiteTitle }}</b>
      </h1>
    </div>
    <div class="flex jc-fe">
      <nuxt-link to="#">
        <b>Quotes</b>
      </nuxt-link>
      <nuxt-link to="#">
        <b>Facts</b>
      </nuxt-link>
      <nuxt-link to="#">
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
.Header a {
  text-decoration: none;
  font-size: 1em;
  color: var(--color-whiteSmoke);
  padding: 1.5em 1.5em 1.5em 1.5em;
  float: right;
  text-shadow: 2px 2px var(--color-black);
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
