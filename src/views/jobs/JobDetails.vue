
<template>

     <div v-if="jb" > 
        <h2>Job Desc</h2>
        <h3>{{ jb.title }}</h3>
        <p>{{ id }}</p>
        <span>{{ jb.details }}</span>
    </div>
    <div v-else>
       <p>loading deatails .....</p>
    </div>
  
</template>

<script>

export default {

  props:['id'],
  // data() {
  //   return {
  //     id: this.$route.params.id 
  //   }
  // }
  data() {
    return {
      jb: null
    } 
  },
  mounted() {
     fetch('http://localhost:5000/jobs/'+this.id)
      .then((res) => res.json()) // this is an callback fun === async
      .then(data => this.jb = data)
      .catch(e => console.log(e.message))
  }

}

</script>
 
