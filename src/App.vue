<template>
  <nav>
    <router-link to="/"> Home </router-link>
    <router-link :to="{name:'About'}" > About </router-link>   
    <router-link :to="{name: 'Jobs'}" > Jobs </router-link>   
   </nav>
   
    <button @click="redirect" >redirect</button>
    <button @click="back" >go back</button>
    <button @click="forword" >go forword</button>

  <router-view/>
</template>


<script>

export default {
  
methods: {
  forword() {
      this.$router.go(1)
    },
    redirect() {
      this.$router.push( { name: 'Home' } )
    },
    back() {
      //go back from history 
    this.$router.go(-1)
    }

  }

}

</script>

<style>

#app { 
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #567ca1;
}
nav {
  padding: 30px;
}
nav a {
  font-weight: bold;
  color: #8ea5bd;
  text-decoration: none;
  margin: 1%;
}
nav a.router-link-exact-active {
  color: #80a795;
  padding: 1%;
  background-color: rgb(221, 212, 200);
  border-radius: 0.6rem;
}
button{
  padding: 1% 2%;
  margin: 3% 1%;
  border: none;
  border-radius: .6rem;
  cursor: pointer;
  text-transform: capitalize;
  
}

</style>
