<template>
  <div class="IndexBlock flex ff-c-w">
    <div class="IndexBlock__introduction" v-if="this.blockPurpose == 'introduction'">
      <h1>
        <b>{{ aboutHeading }}</b>
      </h1>
      <p>
        {{ websiteIntroduction }}
      </p>
    </div>

    <div class="IndexBlock__dailies flex jc-sb ac-c" v-if="this.blockPurpose == 'dailies'">
      <div>
        <h1>
        <b>{{ dailyFactHeading }}</b>
      </h1>
      <div>
        <nuxt-link to="/facts">
          <button type="button">
            <b>{{ viewFactsButton }}</b>
          </button>
        </nuxt-link>
      </div>
      </div>
      <div>
        <h1>
          <b>{{ dailyQuoteHeading }}</b>
        </h1>
        <div>
        <nuxt-link to="/quotes">
          <button type="button">
            <b>{{ viewQuotesButton }}</b>
          </button>
        </nuxt-link>
      </div>
      </div>
    </div>

    <div class="IndexBlock__blog flex jc-c ac-c" v-if="this.blockPurpose == 'blog'">
      <h1>
        <b>{{ blogHeading }}</b>
      </h1>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexBlock',
  props: {
    blockPurpose: String
  },
  data () {
    return {
      aboutHeading: 'What is EarthTrivia?',
      websiteIntroduction: `EarthTrivia is an informative website aiming to inspire and educate through a collection
                            of tidbit style facts and inspirational quotes from some amazing minds and visionaries of
                            the space industry. We also try and keep up to date with all major developments about the 
                            future of Earth and space exploration. These updates are found on our Blog page, the most 
                            recent posts can be found in a section just below this introduction.`,
      dailyFactHeading: 'Fact of the Day',
      dailyQuoteHeading: 'Quote of the Day',
      blogHeading: 'Most Recent Blog Posts',
      viewFactsButton: 'View All Facts',
      viewQuotesButton: 'View All Quotes'
    }
  }
}
</script>

<style type="text/css">
/* stylelint-disable */
.IndexBlock {
  width: 45%;
  padding-top: var(--padding-md);
  padding-bottom: var(--padding-md);
}
.IndexBlock__introduction > p {
  text-align: justify;
  font-size: 1.2em;
}
.IndexBlock__dailies button {
  padding: var(--padding-md) var(--padding-lg);
  background-color: var(--color-white);
  font-family: "Kanit", sans-serif;
  color: var(--color-grey);
}
.IndexBlock > h1 {
  font-family: "Kanit", sans-serif;
  font-weight: 200;
  color: var(--color-grey);
}
.IndexBlock h1:first-of-type {
  text-align: center;
}
.IndexBlock > h4 {
  font-size: 1.5em;
}
.IndexBlock__quickLinks {
  margin-top: 0;
}
</style>
