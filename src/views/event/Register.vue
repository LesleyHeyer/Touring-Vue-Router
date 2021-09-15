<template>
    <p>Register for the event here</p>
    <button @click="register">Register Me</button>
</template>

<script>
export default {
  props: ['event'],

  methods: {
      register() {
          //call APi
          //If registered then redirect to event details


          //when you call <router-link> it's calling this.$router.push from inside the router-link definition
          //ex. When you call <router-link :to="{ name: 'About' }">About</router-link>
             // when it's called it calls this.$router.push({ name: 'About' }) and the route is navigated

          this.$router.push({ //navigate the user to this location
              name: 'EventDetails',
    //the id will be populated by default

                    
                //to navigate without pushing a history entry into the browser: (disabling the back button):

                //this.$router.replace({ name: 'EventDetails', params: {id: 3}})
                //this will repalce the current page with the EventDetails page.
          })
      }
  }
    }

</script>


