<template>
    

    
</template>
<script>
import { defineComponent } from '@vue/composition-api'

export default{
   name: "UserProfile",
   data(){
       return{
            followers: 0,
      user: {
        id: 1,
        username: 'rezowan_ferdous',
        firstname: 'Rezowan',
        lastname: 'Ferdous',
        email: 'rezowan.hossain.tri@gmail.com',
        isAdmin: false ,
        twoot:[
            {id:1 , content: "twitter is amazing "},
            {id:2 , content: " dont forget to subscribe  "}
        ]
      }
       }
   }
}
</script>
