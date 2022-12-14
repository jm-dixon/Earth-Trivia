<template>
  <div class="QuoteReel flex jc-c ac-c ff-r-w">
    <div class="QuoteReel__container flex ff-c-nw" :style="{ backgroundColor: this.loadedQuotes[0].background }">
      <h2>
        {{ loadedQuotes[0].quote }}
      </h2>
      <h3>
        {{ loadedQuotes[0].author }}
      </h3>
    </div>
    <div class="QuoteReel__container flex ff-c-nw" :style="{ backgroundColor: this.loadedQuotes[1].background }">
      <h2>
        {{ loadedQuotes[1].quote }}
      </h2>
      <h3>
        {{ loadedQuotes[1].author }}
      </h3>
    </div>
    <div class="QuoteReel__container flex ff-c-nw" :style="{ backgroundColor: this.loadedQuotes[2].background }">
      <h2>
        {{ loadedQuotes[2].quote }}
      </h2>
      <h3>
        {{ loadedQuotes[2].author }}
      </h3>
    </div>
    <div class="QuoteReel__container flex ff-c-nw" :style="{ backgroundColor: this.loadedQuotes[3].background }">
      <h2>
        {{ loadedQuotes[3].quote }}
      </h2>
      <h3>
        {{ loadedQuotes[3].author }}
      </h3>
    </div>
    <div class="QuoteReel__container flex ff-c-nw" :style="{ backgroundColor: this.loadedQuotes[4].background }">
      <h2>
        {{ loadedQuotes[4].quote }}
      </h2>
      <h3>
        {{ loadedQuotes[4].author }}
      </h3>
    </div>
    <div class="QuoteReel__container flex ff-c-nw" :style="{ backgroundColor: this.loadedQuotes[5].background }">
      <h2>
        {{ loadedQuotes[5].quote }}
      </h2>
      <h3>
        {{ loadedQuotes[5].author }}
      </h3>
    </div>
    <div class="QuoteReel__container flex ff-c-nw" :style="{ backgroundColor: this.loadedQuotes[6].background }">
      <h2>
        {{ loadedQuotes[6].quote }}
      </h2>
      <h3>
        {{ loadedQuotes[6].author }}
      </h3>
    </div>
    <div class="QuoteReel__container flex ff-c-nw" :style="{ backgroundColor: this.loadedQuotes[7].background }">
      <h2>
        {{ loadedQuotes[7].quote }}
      </h2>
      <h3>
        {{ loadedQuotes[7].author }}
      </h3>
    </div>
  </div>
</template>

<script>
// imports
import earthQuotes from '../assets/json/earthQuotes.json'
import spaceQuotes from '../assets/json/spaceQuotes.json'
import siteContent from '../assets/json/siteContent.json'

export default {
  name: 'QuoteReel',
  data () {
    return {
      siteContent,
      quotesArray: [earthQuotes, spaceQuotes],
      loadedQuotes: [
        { id: 0, author: '', quote: '', background: 'var(--color-grey)', color: 'var(--color-lightGrey)' },
        { id: 1, author: '', quote: '', background: 'var(--color-lightGrey)', color: 'var(--color-grey)' },
        { id: 2, author: '', quote: '', background: 'var(--color-grey)', color: 'var(--color-lightGrey)' },
        { id: 3, author: '', quote: '', background: 'var(--color-lightGrey)', color: 'var(--color-grey)' },
        { id: 4, author: '', quote: '', background: 'var(--color-grey)', color: 'var(--color-lightGrey)' },
        { id: 5, author: '', quote: '', background: 'var(--color-lightGrey)', color: 'var(--color-grey)' },
        { id: 6, author: '', quote: '', background: 'var(--color-grey)', color: 'var(--color-lightGrey)' },
        { id: 7, author: '', quote: '', background: 'var(--color-lightGrey)', color: 'var(--color-lightGrey)' }
      ]
    }
  },
  created () {
    this.generateRandomQuote()
  },
  methods: {
    generateRandomQuote () {
      const selectedFile = this.quotesArray[
        Math.floor(
          Math.random() * this.quotesArray.length
        )
      ]
      let counter = 0
      const indexes = []
      while (counter < this.loadedQuotes.length) {
        const index = Math.floor(
          Math.random() * selectedFile.length)
        if (!indexes.includes(index)) {
          indexes.push(index)
          counter++
        }
      }
      counter = 0
      while (counter < this.loadedQuotes.length) {
        const randomQuoteFromFile = selectedFile[indexes[counter]]
        this.loadedQuotes[counter].author = randomQuoteFromFile.author
        this.loadedQuotes[counter].quote = randomQuoteFromFile.quote
        counter++
      }
    }
  }
}
</script>

<style type="text/css">
/* stylelint-disable */
.QuoteReel__container {
  width: 20%;
  text-align: center;
  color: var(--color-whiteSmoke);
}
.QuoteReel__container div {
  width: 100%;
  height: 100%;
}
.QuoteReel h2, h3 {
  padding: var(--padding-lg);
}
</style>
