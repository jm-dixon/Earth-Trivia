<template>
  <div class="Index">
    <index-video />

    <div class="Index__blocks flex jc-c ac-c ff-c-w">
      <index-block
        blockPurpose="Fact of the Day"
        buttonTitle="Read More Facts >"
      />
      <index-block
        blockPurpose="Quote of the Day"
        buttonTitle="View More Quotes >"
      />
      <index-block
        blockPurpose="Latest Blog Post"
        buttonTitle="All Blog Posts >"
      />
    </div>
    <div class="Index__socials">

    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>
