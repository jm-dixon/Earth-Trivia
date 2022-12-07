<template>
  <div class="Header flex jc-fe">
    <nuxt-link to="#">
      Quotes
    </nuxt-link>
    <nuxt-link to="#">
      Facts
    </nuxt-link>
    <nuxt-link to="#">
      Blog
    </nuxt-link>
  </div>
</template>

<script>
export default {
  name: 'AppHeader'
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
</style>
