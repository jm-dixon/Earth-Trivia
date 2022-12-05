<template>
  <div class="QuoteReel flex jc-c ac-c">
    <div class="QuoteReel__container">
      <!-- <p class="QuoteReel__quote">
        {{ quotesArray[0] }}
      </p>
      <h3 class="QuoteReel__author">
        {{ quotesArray[1] }}
      </h3>
      <p>
        {{ numberItem }}
      </p> -->
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
      displayedQuote: null,
      numberItem: null
    }
  },
  mounted () {
    this.quoteSelector()
  },
  methods: {
    generateRandomInteger () {
      let number = Math.random()
      if (number < 0.5) {
        number = 1
      } else {
        number = 0
      }
      return number
    },
    quoteSelector () {
      const file = this.quotesArray[this.generateRandomInteger]
      this.numberItem = file
      // const index = Math.floor(Math.random() * file.length)
      // const quoteFromFile = this.file[index]
    }
  }
}
</script>

<style type="text/css">
/* stylelint-disable */
.QuoteReel__quote {
  padding: var(--padding-md);
  color: var(--color-grey);
}

.QuoteReel__author {
  padding: var(--padding-md);
  color: var(--color-black);
}
</style>
