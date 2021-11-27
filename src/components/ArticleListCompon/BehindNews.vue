<template>
  <span>
    <h2 class="header">
      BEHIND THE NEWS
    </h2>
    <div class="behind">
      <img
        loading="lazy"
        src="https://www.thoughtco.com/thmb/JE0eluqBB-ujkSi4WF4ZXMwI4PY=/510x340/filters:no_upscale():max_bytes(150000):strip_icc()/AB65660-F-57a5b4ef3df78cf459cceae0.jpg"
        alt="thought-image"
        class="behind-image"
      />
      <div class="behind-explain">
        <h3 class="behind-explain-header">WHEN DID EID START IN BANGLADESH</h3>
        <p class="behind-explain-fulltext">
          Around the wourld, eid celebrated most sophisticatedl Lorem ipsum
          dolor sit amet consectetur adipisicing elit. Distinctio, suscipit.
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Doloribus
        </p>
      </div>
    </div>
    <div class="last">
      <div class="last-one">
        <h5>Elementary Education</h5>
        <p>Fun and Qucik Activities and ideas</p>
      </div>
      <div class="last-two">
        <h5>
          Secondary Education
        </h5>
        <p>Natural Ability Grow up</p>
      </div>
    </div>
  </span>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.header {
  margin-left: 40rem;
  font-size: 2.4rem;
  box-sizing: border-box;
  margin-top: 4rem;
}
.behind {
  display: flex;

  &-image {
    display: block;
    height: 30rem;
    width: 30rem;
    border-radius: 50%;
    margin-top: 3rem;
  }
  &-explain {
    margin-left: 5rem;
    &-header {
      font-size: 3rem;
      margin-top: 3rem;
      width: 40%;
    }
    &-fulltext {
      font-size: 2.3rem;
      color: rgb(111, 111, 111);
      margin-top: 1rem;
      width: 60%;
      line-height: 1.5;
    }
  }
}
.last {
  display: flex;
  margin-top: 2rem;
  &-one {
    margin-right: 8.5rem;
  }
  &-one > h5,
  &-two > h5 {
    font-size: 1.3rem;
    color: #757575;
    font-weight: 400;
    letter-spacing: 0.2;
  }
  &-one > p,
  &-two > p {
    font-size: 1.8rem;
    font-weight: 700;
    line-height: 1.2;
  }
}
</style>
