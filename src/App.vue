<template>
  <nav>
    <router-link to="/"> Home </router-link>
    <router-link :to="{name:'About'}" > About </router-link>   
    <router-link :to="{name: 'Jobs'}" > Jobs </router-link>   
   </nav>
  <router-view/>
</template>

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

</style>
