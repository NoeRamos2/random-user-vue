<template>
  <div>
    <div class="col text-center" id="details">
      <h2>User Details</h2>
      <div v-if="user.picture">
        <img :src="user.picture.large" />
        <br>
        <i class="bi bi-person-circle" >
          Hi, My name is {{ user.name.first }} {{ user.name.last }}
        </i><br>
        <i class="bi bi-envelope-fill">
          My email address is {{ user.email }}
        </i><br>
        <i class="bi bi-geo-alt-fill">
          My location is {{ user.location.city}} , {{user.location.country}}
        </i><br>
       <i class="bi bi-telephone-fill">
         My phone number is {{user.phone}}
       </i><br>
       <i class="bi bi-key-fill">
         Login info username: {{user.login.username}} - password: {{user.login.password}} 
       </i>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Details",
  props: {
    user: {
      type: Object,
      default: () => {},
    },
  },
  data() {
    return {
      //user: {}
    };
  },
};
</script>

<style>
.bi{
  font-size: 1.5rem; 
  color: #ffffff;
}
#details{
  background-color: #62727b;
  color: #ffffff;
  margin: 1em;
  font-size: 1.5rem; 
}
</style>