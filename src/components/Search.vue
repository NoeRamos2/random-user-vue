<template>
  <div>
    <div class="container border border-primary" id="search">
      <div class="row">
        <div class="col col-5"></div>
        <div class="col col 2">
          <br>
           <form action="">
             <div class="form-check" >
              <input class="form-check-input" v-model="gender" type="radio" name="flexRadioDefault" value="male" id="flexRadioDefault1">
              <label class="form-check-label" for="flexRadioDefault1">
                Male
              </label>
            </div>
            <div class="form-check">
              <input class="form-check-input" v-model="gender" type="radio" name="flexRadioDefault" value="female" id="flexRadioDefault2">
              <label class="form-check-label" for="flexRadioDefault2">
                Female
              </label>
            </div>
             <button type="submit" class="btn btn-primary" @click="searchUser">Search</button>
           </form>
        </div>
        <div class="col col-5"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Search",
  props: {},
  data(){
    return {
      ms: "enviado",
      gender: "male"
    }
  },
  methods:{
    searchUser(e){
      e.preventDefault();
      this.$emit("click",this.gender);
    }
  }
};
</script>

<style>
#search{
  background-color: #62727b;
  color: #ffffff;
  margin: 1em;
}
</style>