<template>
  <div class="IndexBlock flex ff-c-w">
    <h1>
      {{ blockPurpose }}
    </h1>
    <p>
      {{ siteDescription }}
    </p>
    <h3>
      {{ descriptionSubTitle }}
    </h3>
    <p>{{ quickLinks[0] }} | {{ quickLinks[1] }} | {{ quickLinks[2] }}</p>
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
      siteDescription: `Earth Trivia is an informative website about planet Earth and the solar system.
                        This site aims to educate and inspire with titbit style facts, quotes from truly
                        amazing minds and blog posts and recent developments relating to our planet or
                        space exploration.

                        This site is linked directly to the Facebook page @EarthTrivia. All posts here will be
                        echoed on the page at the same time and vice versa.

                        This site is a personal project taken live, as such it is moneiized through the use of
                        Google Adsense to help with running costs, upkeep and any future developments to the site.`,
      descriptionSubTitle: 'Quick Links',
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
}
</style>
