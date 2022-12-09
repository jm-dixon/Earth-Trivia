<template>
  <div class="IndexBlock flex ff-c-w">
    <h1>
      {{ siteContent.aboutTitle }}
    </h1>
    <p>
      {{ siteContent.aboutDescription }}
    </p>
    <h4>
      {{ siteContent.aboutSubTitle }}
    </h4>
    <p class="IndexBlock__quickLinks">
      <nuxt-link to="#">
        {{ quickLinks[0] }} >
      </nuxt-link>
    </p>
    <p class="IndexBlock__quickLinks">
      <nuxt-link to="#">
        {{ quickLinks[1] }} >
      </nuxt-link>
    </p>
    <p class="IndexBlock__quickLinks">
      <nuxt-link to="#">
        {{ quickLinks[2] }} >
      </nuxt-link>
    </p>
  </div>
</template>

<script>
// imports
import siteContent from '../assets/json/siteContent.json'

export default {
  name: 'IndexBlock',
  data () {
    return {
      siteContent,
      quickLinks: ['Quotes', 'Facts', 'Blog Posts']
    }
  }
}
</script>

<style type="text/css">
/* stylelint-disable */
.IndexBlock {
  width: 40%;
  padding-top: var(--padding-md);
  padding-bottom: var(--padding-md);
}
.IndexBlock p {
  white-space: pre-line;
  margin: 0;
}
.IndexBlock h1, h4 {
  margin-bottom: 0;
}
.IndexBlock h4 {
  font-size: 1.5em;
}
.IndexBlock__quickLinks {
  margin: 0;
}
</style>
