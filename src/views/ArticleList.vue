<template>
  <div>
    <hr class="border-top" />
    <div class="primary">
      <div>
        <img
          class="primary_sub-main-card-logo small-margin"
          src="https://www.thoughtco.com/static/3.64.0/image/hp-science,tech,math.png"
          alt="science logo"
        />
      </div>
      <div>
        <img
          class="primary_sub-main-card-logo small-margin"
          src="https://www.thoughtco.com/static/3.64.0/image/hp-humanities.png"
          alt="science logo"
        />
      </div>
      <div>
        <img
          class="primary_sub-main-card-logo small-margin"
          src="https://www.thoughtco.com/static/3.64.0/image/hp-languages.png"
          alt="science logo"
        />
      </div>
      <div>
        <img
          class="primary_sub-main-card-logo small-margin"
          src="https://www.thoughtco.com/static/3.64.0/image/hp-resources.png"
          alt="science logo"
        />
      </div>
    </div>
    <div class="primary">
      <!-- <p>{{ article[0].id }}</p>
     <p>PrimaryContent</p>
    <div v-for="art in article" :key="art.id">
      <li v-if=art.type = 'science' @click="toFullArticle">{{ art.header }}</li>
    </div>
    <p>I am mohtasim.</p>
      -->
      <div class="primary_sub">
        <div class="primary_sub-main">
          <div class="primary_sub-main-card">
            <router-link to="/section-list/science">
              <h3 class="primary_sub-main-card-header">
                Science,Tech,Math
              </h3></router-link
            >
            <!-- science sub logo -->
            <img
              src="https://www.thoughtco.com/thmb/G5bfGcnsEuoKerwsCmiPxd8-cOU=/337x0/filters:no_upscale():max_bytes(150000):strip_icc():format(webp)/silicone-baking-molds-5ae27a9143a1030036784001.jpg"
              alt="science sub logo"
              class="science-sub-logo"
            />

            <!-- grid layout -->
            <div class="primary_sub-main-card-grid">
              <router-link-to
                v-for="art in article"
                :key="art.id"
                :id="art.id"
                resources="science"
                :type="art.type"
                :header="art.header"
              ></router-link-to>
            </div>
            <hr />
          </div>
        </div>
      </div>
      <div class="primary_sub">
        <div class="primary_sub-main">
          <div class="primary_sub-main-card">
            <router-link to="/section-list/humanities">
              <h3 class="primary_sub-main-card-header">
                Humanities
              </h3></router-link
            >
            <img
              src="https://www.thoughtco.com/thmb/G5bfGcnsEuoKerwsCmiPxd8-cOU=/337x0/filters:no_upscale():max_bytes(150000):strip_icc():format(webp)/silicone-baking-molds-5ae27a9143a1030036784001.jpg"
              alt="science sub logo"
              class="science-sub-logo"
            />
            <div class="primary_sub-main-card-grid">
              <router-link-to
                v-for="art in article"
                :key="art.id"
                :id="art.id"
                resources="humanities"
                :type="art.type"
                :header="art.header"
              ></router-link-to>
            </div>
          </div>
        </div>
      </div>
      <div class="primary_sub">
        <div class="primary_sub-main">
          <div class="primary_sub-main-card">
            <router-link to="/section-list/language">
              <h3 class="primary_sub-main-card-header">
                Languages
              </h3></router-link
            >
            <img
              src="https://www.thoughtco.com/thmb/G5bfGcnsEuoKerwsCmiPxd8-cOU=/337x0/filters:no_upscale():max_bytes(150000):strip_icc():format(webp)/silicone-baking-molds-5ae27a9143a1030036784001.jpg"
              alt="science sub logo"
              class="science-sub-logo"
            />
            <div class="primary_sub-main-card-grid">
              <!-- <router-link to="/">
                <div v-if="art.type == 'language'">
                  <h2 class="small">{{ art.type }}</h2>
                  <h2 class="big">{{ art.header }}</h2>
                </div>
              </router-link> -->
              <router-link-to
                v-for="art in article"
                :key="art.id"
                :id="art.id"
                resources="language"
                :type="art.type"
                :header="art.header"
              ></router-link-to>
            </div>
          </div>
        </div>
      </div>
      <div class="primary_sub">
        <div class="primary_sub-main">
          <div class="primary_sub-main-card">
            <router-link to="/section-list/resources">
              <h3 class="primary_sub-main-card-header">
                Resources
              </h3></router-link
            >
            <img
              src="https://www.thoughtco.com/thmb/G5bfGcnsEuoKerwsCmiPxd8-cOU=/337x0/filters:no_upscale():max_bytes(150000):strip_icc():format(webp)/silicone-baking-molds-5ae27a9143a1030036784001.jpg"
              alt="science sub logo"
              class="science-sub-logo"
            />

            <div>
              <div class="primary_sub-main-card-grid">
                <!-- <router-link :to="articleDetailLink">
                  <div v-if="art.type == 'resources'">
                    <h2 class="small">{{ art.type }}</h2>
                    <h2 class="big">
                      {{ art.header }}
                    </h2>
                  </div>
                </router-link> -->
                <router-link-to
                  v-for="art in article"
                  :key="art.id"
                  :id="art.id"
                  resources="resources"
                  :type="art.type"
                  :header="art.header"
                ></router-link-to>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <email-card></email-card>
  <behind-news></behind-news>
</template>

<script>
// @ is an alias to /src
import RouterLinkTo from "../components/ArticleListCompon/RouterLinkTo";
import EmailCard from "../components/ArticleListCompon/EmailCard";
import BehindNews from "../components/ArticleListCompon/BehindNews";
export default {
  components: {
    RouterLinkTo,
    EmailCard,
    BehindNews,
  },
  computed: {
    article() {
      return this.$store.getters["article/articles"];
    },
  },
};
</script>

<style lang="scss">
@import "../assets/styles/abstracts/_mixins.scss";
.border-middle {
  border-bottom: 1px solid #c4c4c4;
  // padding-bottom: 2rem;
}
.border-top {
  border-top: 3px solid #232323;
}
a {
  text-decoration: none;
}

.primary {
  display: grid;
  justify-content: space-evenly;
  grid-template-columns: repeat(4, 1fr);
  // column-gap: 0.5rem;
  background-color: rgb(241, 241, 241);
  margin-top: -0.2rem; // for solid line after heading
  color: #232323;
  &_sub {
    height: auto;
    justify-self: center;
    width: 27.3rem;
    z-index: 0;

    &-main-card {
      background-color: rgb(255, 255, 255);
      padding: 1rem;
      z-index: 0;

      &-logo {
        display: block;
        height: 11.3rem;
        width: 19rem;
        margin: 0 auto;
      }
      &-header {
        text-align: center;
        color: #282828;
        font-size: 2rem;
        padding: 2rem 0;
      }
    }
  }
}
.small {
  font-size: 1.2rem;
  padding-top: 1rem;
  // columns: inherit;
  color: #8a8a8a;
}
.small-margin {
  margin-top: 5.4rem;
  z-index: 5;
}
.big {
  font-size: 2.2rem;
  padding-bottom: 1rem;
  color: #232323;
}
.science-sub-logo {
  display: block;
  margin: 0 auto;
  height: 16.9rem;
  width: 25.3rem;
}
</style>
