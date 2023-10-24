<template>
  <h2>Jobs .... </h2>
  <h4 v-for=" jb in jobs " :key="jb.id" class="jobs"> 
      <!-- <h5>{{ jb.title }}</h5> -->
      <router-link :to="{name:'JobDetails' , params:{id:jb.id}}"> 
        <h5>{{ jb.title }}</h5>
      </router-link>
  </h4>
</template>

<script>
export default {

  name:'Jobs',

  data() {
    return {
      jobs: [
        // {title:"web" , id:1 , details: "lorem" },
        // {title:"design" , id:2 , details: "lorem" },
        // {title: "UI", id:3 , details: "lorem"  }
     ]
   }
  },
  mounted() {
    //asynchrones -- promes
    fetch('http://localhost:5000/jobs')
      .then((res) => res.json()) // this is an callback fun === async
      .then(data => this.jobs = data)
      .catch( e=> console.log(e.message ) )
  }
  
}
</script>


<style>

a{
  text-decoration: none;
}
.jobs{
  display: flex;
  flex-direction: column;
  background-color: rgb(162, 169, 150);
  color: rgb(129, 10, 10);
  font-size: 22px;
  width: 30%;
  padding: 1%;
  margin: 1% auto;
  border-radius: 2rem;
}
.jobs:hover{
  background-color: rgb(175, 203, 119);
  color: rgb(129, 10, 10);
}

</style>

 