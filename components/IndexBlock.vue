<template>
  <div class="IndexBlock flex ff-r-w">
    <div class="IndexBlock__title">
      <h1>
        {{ blockPurpose }}
      </h1>
      <button type="button">
        {{ buttonTitle }}
      </button>
    </div>
    <div class="IndexBlock__feature">

    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexBlock',
  props: {
    blockPurpose: String,
    buttonTitle: String
  }
}
</script>

<style type="text/css">
/* stylelint-disable */
.IndexBlock {
  width: 60%;
  padding-top: var(--padding-md);
  padding-bottom: var(--padding-md);
}
.IndexBlock div {
  width: 45%;
}
.IndexBlock__title button {
  background-color: transparent;
  border: none;
}
.IndexBlock__feature {
  border: 2px solid var(--color-black);
  padding: var(--padding-md);
}
</style>
