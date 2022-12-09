<template>
  <div class="QuoteReel flex jc-c ac-c ff-r-w">
    <div v-for="item in loadedQuotes" v-bind:key="item.id" :style="{ backgroundColor: item.background, color: item.color }">
      <h2>
        {{ item.quote }}
      </h2>
      <h2>
        {{ item.author }}
      </h2>
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
        { id: '0', author: 'test', quote: 'test', background: 'var(--color-grey)', color: 'var(--color-neruoscriptBlue)' },
        { id: '1', author: 'test', quote: 'test', background: 'var(--color-whiteSmoke)', color: 'var(--color-grey)' },
        { id: '2', author: 'test', quote: 'test', background: 'var(--color-lightGrey)', color: 'var(--color-black)' },
        { id: '3', author: 'test', quote: 'test', background: 'var(--color-neruoscriptBlue)', color: 'var(--color-lightGrey)' },
        { id: '4', author: 'test', quote: 'test', background: 'var(--color-lightGrey)', color: 'var(--color-black)' },
        { id: '5', author: 'test', quote: 'test', background: 'var(--color-neruoscriptBlue)', color: 'var(--color-lightGrey)' },
        { id: '6', author: 'test', quote: 'test', background: 'var(--color-lightGrey)', color: 'var(--color-black)' },
        { id: '7', author: 'test', quote: 'test', background: 'var(--color-neruoscriptBlue)', color: 'var(--color-lightGrey)' },
        { id: '8', author: 'test', quote: 'test', background: 'var(--color-grey)', color: 'var(--color-neruoscriptBlue)' },
        { id: '9', author: 'test', quote: 'test', background: 'var(--color-whiteSmoke)', color: 'var(--color-grey)' }
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
.QuoteReel h2, h3 {
  padding: var(--padding-lg);
}
</style>
