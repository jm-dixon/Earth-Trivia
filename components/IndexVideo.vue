<template>
  <div class="IndexVideo">
    <video autoplay muted loop>
      <source src="../static/titleVideo.mp4" type="video/mp4">
    </video>

    <div class="IndexVideo__titleBox flex jc-c ac-c ai-c ff-c-w">
      <h1>
        <b>Quote Here</b>
      </h1>
      <h3>
        <b>Author Here</b>
      </h3>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexVideo',
  data () {
    return {
      titleQuote: null
    }
  },
  created () {
    // this.chooseRandomQuote()
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
  font-family: "Kanit", sans-serif;
}
.IndexVideo__titleBox h3 {
  color: var(--color-neruoscriptBlue);
  font-size: 2em;
  text-shadow: 2px 2px var(--color-black);
  margin-top: 0;
}
</style>
