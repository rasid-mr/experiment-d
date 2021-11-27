<template>
  <div class="email">
    <form @submit.prevent="formSubmit" class="email-form">
      <label for="email"
        ><h2 class="email-header">Learn Something New Everyday</h2></label
      >
      <input
        id="email"
        type="text"
        placeholder="Enter Your Email"
        class="email-input"
      />
      <div class="sign">
        <button class="email-button">Sign up</button>
      </div>
    </form>
    <div class="email-image">
      <img
        src="https://www.thoughtco.com/static/3.66.0/image/newsletter.png"
        alt="thoughtco"
        class="email-image-1"
      />
    </div>
    <div class="follow">
      <label for="icon" class="follow-us">Follow Us</label>
      <legend class="follow-social">
        <i id="icon" class="fab fa-facebook-f follow-social-facebook"></i>
        <i id="icon" class="fab fa-flipboard follow-social-flipboard"></i>
      </legend>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.follow {
  margin-left: 9.5rem;
  margin-top: 4rem;
  font-size: 2.1rem;
  font-weight: 700;
  &-social {
    display: flex;

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
.email-image {
  &-1 {
    display: block;
    height: auto;
    margin-left: 25rem;
    margin-top: 1.1rem;
    width: 17.5rem;
  }
}
.email {
  width: 120rem;
  height: 14.846rem;
  background-color: #e5ddcf;
  margin: 2rem 0;
  padding: 1.12rem 2.56rem;
  box-sizing: border-box;
  display: flex;

  &-header {
    font-size: 1.8rem;
    color: #282828;
    font-weight: 1200;
    margin-top: 3rem;
  }
  &-input {
    width: 53.334rem;
    height: 4.2rem;
    padding: 0.94rem 1.04rem;
    font-size: 2rem;
  }
  &-button {
    height: 4.15rem;
    // padding: 1.4rem 1.04rem;
    width: 10.66rem;
    font-size: 1.6rem;
    color: #cccccc;
    background-color: #c41e24;
    outline: none;
    cursor: pointer;
    border: none;
    position: absolute;
    top: 93.6rem;
    left: 71.7rem;
  }
}
</style>
