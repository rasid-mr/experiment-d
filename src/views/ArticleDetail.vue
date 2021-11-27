<template>
  <div>
    <div class="parent">
      <div>
        <p class="parent_type">
          {{ product.type }} <span class="parent_type-arrow">></span>
          {{ product.subtype }}
        </p>
        <h1 class="parent_header">{{ product.header }}</h1>
        <img :src="image" alt="article-hero-imgae" class="parent-image" />
        <p class="parent_date">{{ date }}</p>
        <p class="parent_fulltext">{{ product.fullText }}</p>
      </div>
    </div>
    <div class="bottom">
      <div v-for="section in sectionData" :key="section.id">
        <secondary-header
          class="bottom-secondary-header"
          :header="section.header"
          :typeId="section.type"
          :idOne="section.id"
          :image="section.imageLink"
        ></secondary-header>
      </div>
    </div>
  </div>
</template>

<script>
import SecondaryHeader from "../components/SectionListCompon/SecondaryHeader";
export default {
  components: {
    SecondaryHeader,
  },
  props: ["id"],
  data() {
    return {
      selectedArticle: null,
      selectedArticleSec: null,
      selectedSection: null,
    };
  },
  computed: {
    // product() {
    //   return (this.selectedArticle = this.$store.getters[
    //     "article/articles"
    //   ].find((a) => a.id == this.id));
    // },
    // header() {
    //   return this.product.header;
    // },
    comId() {
      return this.$route.params.id;
    },
    sectionData() {
      return (this.selectedSection = this.$store.getters[
        "article/articles"
      ].filter((a) => a.type == this.$route.query.type));
    },
    product() {
      console.log(this.$route.query.type);
      return (this.selectedArticleSec = this.$store.getters[
        "article/articles"
      ].find((a) => a.id == this.$route.params.id));
    },
    image() {
      return this.product.imageLink;
    },
    date() {
      return new Date().toISOString();
    },
  },

  methods: {},
};
</script>

<style scoped lang="scss">
.bottom {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
.parent {
  &_type {
    color: red;
    font-size: 1.2rem;
    font-weight: 600;
    &-arrow {
      vertical-align: middle;
    }
  }
  &_header {
    font-size: 4rem;
    color: rgb(27, 27, 27);
  }
  &-image {
    display: block;
    height: 50rem;
    width: 80rem;
    object-fit: cover;
  }
  &_date {
    margin-top: 4rem;
    font-size: 2rem;
  }
  &_fulltext {
    font-size: 1.8rem;
    margin-top: 5rem;
  }
}
</style>
