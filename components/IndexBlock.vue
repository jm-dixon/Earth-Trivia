<template>
  <div class="IndexBlock flex ff-c-w">
    <div v-if="this.blockPurpose == 'introduction'">
      <h1>
        <b>{{ siteContent.indexHeading }}</b>
      </h1>
    </div>

    <div class="IndexBlock__dailies flex jc-sb ac-c" v-if="this.blockPurpose == 'dailies'">
      <h1>
        <b>{{ siteContent.dailyFactHeading }}</b>
      </h1>
      <h1>
        <b>{{ siteContent.dailyQuoteHeading }}</b>
      </h1>
    </div>
  </div>
</template>

<script>
// imports
import siteContent from '../assets/json/siteContent.json'

export default {
  name: 'IndexBlock',
  props: {
    blockPurpose: String
  },
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
.IndexBlock > h1 {
  font-family: "Kanit", sans-serif;
  font-weight: 200;
  color: #272727;
}
.IndexBlock h1:first-of-type {
  text-align: center;
}
.IndexBlock > p {
  white-space: pre-line;
}
.IndexBlock > h4 {
  font-size: 1.5em;
}
.IndexBlock {
  width: 40%;
  padding-top: var(--padding-md);
  padding-bottom: var(--padding-md);
}
.IndexBlock__quickLinks {
  margin-top: 0;
}
</style>
