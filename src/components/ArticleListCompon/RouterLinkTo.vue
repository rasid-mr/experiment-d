<template>
  <div v-if="type == resources && number <= 4">
    <h2 class="small uppercase">{{ type }}</h2>
    <router-link :to="articleDetailLink"   
      ><h2 class="big big-header">
        {{ header }}
      </h2></router-link
    >
  </div>
  <!-- <div v-for="index in ten" :key="index"> 
    {{index }}
    <span>what is this</span>
  </div> -->

</template>

<script>
export default {
  props: ["id", "type", "resources", "header", "number"],

 

  computed: {
    articleDetailLink() {
      return this.$route.path + "/" + this.id;
    },
  },

  
};
</script>

<style scoped>
 
.big-header {
  font-weight: 400;
  line-height: 1.3;
  color: rgb(22, 22, 22);
}
 
 

</style>
