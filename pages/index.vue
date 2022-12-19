<template>
  <div class="Index">
    <index-video />

    <div class="Index__blocks flex jc-c ac-c ff-c-w">
      <index-block
        blockPurpose="introduction"
      />
      <index-block
        blockPurpose="dailies"
      />
      <index-block
        blockPurpose="blog"
      />
    </div>

    <div class="Index__socials">
      <index-block
        blockPurpose="socials"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>
