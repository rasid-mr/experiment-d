<template>
  <div v-if="type == resources">
    <h2 class="small">{{ type }}</h2>
    <router-link :to="articleDetailLink"
      ><h2 class="big">
        {{ header }}
      </h2></router-link
    >
  </div>
</template>

<script>
export default {
  props: ["id", "type", "resources", "header"],

  computed: {
    articleDetailLink() {
      return this.$route.path + "/" + this.id;
    },
  },
};
</script>

<style></style>
