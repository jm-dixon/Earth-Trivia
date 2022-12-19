<template>
    <div class="Footer flex">
      <div>
        <p>
          <b>EarthTrivia &copy; 2022</b>
        </p>
      </div>
      <div>
        <ul>
          <a target="blank" href="https://www.nasa.gov/">
            <li>NASA Website</li>
          </a>
          <a target="blank" href="https://twitter.com/nasa">
            <li>NASA Twitter</li>
          </a>
        </ul>
      </div>
      <div>
        <ul>
          <a target="blank" href="https://www.facebook.com/EarthTrivia">
            <li>Facebook Page</li>
          </a>
        </ul>
      </div>
    </div>
  </template>

<script>
export default {
  name: 'AppFooter'
}
</script>

<style type="text/css">
/* stylelint-disable */
.Footer {
  background-color: var(--color-neruoscriptBlue);
  padding: var(--padding-md);
}
.Footer p {
  font-family: "Kanit", sans-serif;
  color: var(--color-grey);
}
.Footer li {
  text-decoration: none;
  font-family: "Kanit", sans-serif;
  list-style: none;
  color: var(--color-grey);
  font-weight: 400;
}
</style>
