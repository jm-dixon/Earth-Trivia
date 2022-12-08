<template>
  <div class="QuoteReel flex jc-c ac-c">
    <div v-for="item in loadedQuotes" v-bind:key="item.id" :style="{ backgroundColor: item.background }">
      <h2>
        {{ item.quote }}
      </h2>
      <h3>
        {{ item.author }}
      </h3>
    </div>
  </div>
</template>

<script>
// imports
import earthQuotes from '../assets/json/earthQuotes.json'
import spaceQuotes from '../assets/json/spaceQuotes.json'

export default {
  name: 'QuoteReel',
  data () {
    return {
      quotesArray: [earthQuotes, spaceQuotes],
      loadedQuotes: [
        { id: '0', author: 'test', quote: 'test', background: 'transparent' },
        { id: '1', author: 'test', quote: 'test', background: 'transparent' },
        { id: '2', author: 'test', quote: 'test', background: 'transparent' },
        { id: '3', author: 'test', quote: 'test', background: 'transparent' },
        { id: '4', author: 'test', quote: 'test', background: 'transparent' },
        { id: '5', author: 'test', quote: 'test', background: 'transparent' },
        { id: '6', author: 'test', quote: 'test', background: 'transparent' },
        { id: '7', author: 'test', quote: 'test', background: 'transparent' },
        { id: '8', author: 'test', quote: 'test', background: 'transparent' },
        { id: '9', author: 'test', quote: 'test', background: 'transparent' }
      ]
    }
  }
}
</script>

<style type="text/css">
/* stylelint-disable */
.QuoteReel div {
  width: 20%;
  text-align: center;
  color: var(--color-whiteSmoke);
}
</style>
