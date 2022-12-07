<template>
  <div class="IndexVideo">
    <video autoplay muted loop>
      <source src="../static/titleVideo.mp4" type="video/mp4">
    </video>

    <div class="IndexVideo__titleBox flex jc-c ac-c ai-c ff-c-w">
      <h1>"{{ titleQuote.quote }}"</h1>
      <h3>{{ titleQuote.author }}</h3>
    </div>
  </div>
</template>

<script>
// imports
import earthQuotes from '../assets/json/earthQuotes.json'
import spaceQuotes from '../assets/json/spaceQuotes.json'

export default {
  name: 'IndexVideo',
  data () {
    return {
      quotesArray: [earthQuotes, spaceQuotes],
      titleQuote: null
    }
  },
  created () {
    this.chooseRandomQuote()
  },
  methods: {
    chooseRandomQuote () {
      const selectedFile = this.quotesArray[
        Math.floor(
          Math.random() * this.quotesArray.length
        )
      ]
      const randomQuoteFromFile = selectedFile[
        Math.floor(
          Math.random() * selectedFile.length
        )
      ]
      this.titleQuote = randomQuoteFromFile
    }
  }
}
</script>

<style type="text/css">
/* stylelint-disable */
.IndexVideo {
  position: relative;
}
.IndexVideo video {
  width: 100%;
  opacity: 0.9;
}
.IndexVideo__titleBox {
  position: absolute;
  top: 0;
  width: 100%;
  height: 100%;
  text-align: center;
}
.IndexVideo__titleBox h1 {
  color: var(--color-whiteSmoke);
  max-width: 50%;
  font-size: 2.5em;
  text-shadow: 2px 2px var(--color-black);
}
.IndexVideo__titleBox h3 {
  color: var(--color-whiteSmoke);
  font-size: 1.5em;
  text-shadow: 2px 2px var(--color-black);
}
</style>
