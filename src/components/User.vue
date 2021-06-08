<template>
  <div class="container" id="user">
    <h2 class="p-2">Vue-Cli with Bootstrap and Random User API</h2>
    <div class="container">
      <h3>Search Random User and load details</h3>
      <br>
      <button type="button" class="btn btn-primary" @click="getUser">
        Search
      </button>
      <br>
    </div>
    <div class="container">
      <Details v-bind:user="user"></Details>
    </div>
    <div class="container">
      <Search @click="searchUser"></Search>
    </div>
  </div>
</template>

<script>
import Details from "./Details.vue";
import Search from "./Search.vue";

export default {
  name: "User",
  components: {
    Details,
    Search,
  },
  props: {},
  data() {
    return {
      user: {},
    };
  },
  mounted() {
    //this.getUser();
  },
  methods: {
    getUser() {
      fetch("https://randomuser.me/api/")
        .then((response) => {
          return response.json();
        })
        .then((data) => {
          this.user = data.results[0];
          console.log("user get user", this.user);
        });
    },
    searchUser(ms){
      console.log("search",ms);
    }
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
#user{
  background-color:#263238;
  color: #ffffff;
}
</style>
