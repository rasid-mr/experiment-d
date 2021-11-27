<template>
  <footer>
    <div class="footer">
      <div class="footer-logo">
        <h1>Thought<span class="footer-logo-sub">Co.</span></h1>
        <form @submit.prevent="formSubmit" class="footer-email-form">
          <label for="footer-email"
            ><h2 class="footer-email-header">
              Learn Something New Everyday
            </h2></label
          >
          <div class="footer-inside-form">
            <input
              id="footer-email"
              type="text"
              placeholder="Enter Your Email"
              class="footer-email-input"
            />
            <button class="footer-email-button">Sign up</button>
          </div>
        </form>
        <div class="footer-follow">
          <label for="icon" class="footer-follow-us">Follow Us</label>
          <legend class="footer-follow-social">
            <i
              id="icon"
              class="fab fa-facebook-f footer-follow-social-facebook"
            ></i>
            <i
              id="icon"
              class="fab fa-flipboard footer-follow-social-flipboard"
            ></i>
          </legend>
        </div>
      </div>
      <div class="footer-section">
        <router-link to="/section-list/science" class="routerHyperLink"
          ><h2 class="footer-section_science">
            Science,Tech,Math
          </h2></router-link
        >
        <router-link to="/section-list/humanities" class="routerHyperLink">
          <h2 class="footer-section_humanities">Humanities</h2></router-link
        >
        <router-link to="/section-list/language" class="routerHyperLink">
          <h2 class="footer-section_languages">Languages</h2></router-link
        >
        <router-link to="/section-list/resources" class="routerHyperLink">
          <h2 class="footer-section_resources">Resources</h2></router-link
        >
      </div>
    </div>
    <div class="footer-dotdash">
      <h1 class="footer-dotdash-header">DotDash</h1>
      <p class="footer-dotdash-fullText">
        ThoughtCo is part of the Dotdash publishing family.
      </p>
    </div>
  </footer>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.footer-dotdash {
  padding: 2rem 0;
  font-size: 1.5rem;
  display: flex;
  align-items: center;

  &-header {
    font-weight: 200;
  }

  &-fullText {
    margin-top: 0.7rem;
    margin-left: 1rem;
  }
}
.routerHyperLink {
  text-decoration: none;
  color: black;
}
.footer-section {
  margin-top: 7.5rem;
  margin-left: 4rem;
  font-size: 1.2rem;

  & * {
    margin-bottom: 1.2rem;
    color: white;
  }
}
.footer {
  margin-top: 10rem;
  color: white;
  background-color: #333;
  height: 24rem;
  display: flex;

  &-inside-form {
    display: flex;
  }
  &-email-header {
    font-size: 2rem;
    margin: 1rem 0;
  }
  &-email-input {
    width: 53.334rem;
    height: 4.2rem;
    padding: 0.94rem 1.04rem;
    font-size: 2rem;
  }
  &-email-button {
    font-size: 1.6rem;
    color: #cccccc;
    background-color: #c41e24;
    outline: none;
    cursor: pointer;
    border: none;
    width: 10.6rem;
  }

  &-follow {
    margin-top: 1rem;
  }

  &-follow-social {
    display: flex;
    margin: 1rem 0;

    &-facebook {
      color: rgb(255, 255, 255);
      background-color: #344e86;
      display: flex;
      width: 4.2rem;
      height: 4.2rem;
      justify-content: center;
      align-items: center;
      cursor: pointer;

      &:focus {
        background-color: #578b9e;
      }
    }
    &-flipboard {
      margin-left: 0.4rem;
      color: white;
      background-color: rgb(225, 2, 2);
      display: flex;
      width: 4.2rem;
      height: 4.2rem;
      justify-content: center;
      align-items: center;
      cursor: pointer;

      &:focus {
        background-color: rgb(182, 5, 5);
      }
    }
  }
}
.footer-logo {
  font-size: 2.5rem;
  &-sub {
    color: #ffe186;
  }
}
</style>
