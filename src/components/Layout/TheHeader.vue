<template>
  <header class="header">
    <router-link to="/" class="routerHyperLink">
      <h2 class="header_logo">
        Thought<span class="header_logo-sub">Co.</span>
      </h2></router-link
    >
    <router-link to="/section-list/science" class="routerHyperLink"
      ><h2 class="header_science">Science,Tech,Math</h2></router-link
    >
    <router-link to="/section-list/humanities" class="routerHyperLink">
      <h2 class="header_humanities">Humanities</h2></router-link
    >
    <router-link to="/section-list/language" class="routerHyperLink">
      <h2 class="header_languages">Languages</h2></router-link
    >
    <router-link to="/section-list/resources" class="routerHyperLink">
      <h2 class="header_resources">Resources</h2></router-link
    >
    <router-link to="/about" class="routerHyperLink">
      <h2 class="header_about">About Us</h2></router-link
    >
    <router-link to="/" class="routerHyperLink">
      <h2 class="header_searchIcon">search</h2></router-link
    >
  </header>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
* {
  box-sizing: border-box;
}
.routerHyperLink {
  text-decoration: none;
  color: black;
}
.header {
  text-decoration: none;
  height: 5rem;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  padding: 4rem 0;

  & > *:not(:first-child) {
    font-size: 1.2rem;
  }

  & > :hover {
    color: #ffe186;
    transition: 0.3s all;
  }

  &_logo {
    font-size: 4rem;
    justify-self: stretch;
    margin-top: -0.4rem;
    &-sub {
      color: #ffe186;
    }
  }
  &_searchIcon {
    margin-left: 10rem;
  }
}
</style>
