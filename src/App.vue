<template>
  <div id="app" class="div">
    {{ user.username }} - {{fullname}}
    <br>

    <strong> Followers  </strong> {{followers}}
    <button class="btn btn-info" @click="followerUser">
      Follower ADD + 
    </button>
    <button class="btn" @click="subtractfollower"> 
      Follower Sub -
    </button>
    <br>
    <div v-if="user.isAdmin">
        Admin
    </div>
  </div>

</template>

<script>

export default {
  name: 'App',
  // components:{twoot,User},
  data() {
    return {
      followers: 0,
      user: {
        id: 1,
        username: 'rezowan_ferdous',
        firstname: 'Rezowan',
        lastname: 'Ferdous',
        email: 'rezowan.hossain.tri@gmail.com',
        isAdmin: false 
      }
    }

    },
    watch: {
      followers( newfollowercount,oldfollowercount){
        if (oldfollowercount< newfollowercount){
          console.log(`${this.user.username} has gained a follower `)
        }
      }
    },
    computed:{
      fullname() {
        return `${this.user.firstname} ${this.user.lastname}`
      }
    },
    methods:{
      followerUser(){
        this.followers++
      },
      subtractfollower(){
        this.followers--
      }
    },
    mounted(){
      this.followerUser();

    }
  }
  
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
