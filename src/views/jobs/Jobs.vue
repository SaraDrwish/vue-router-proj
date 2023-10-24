<template>
  <h2>jobs page </h2>
  <h4 v-for=" jb in jobs " :key="jb.id" > 
      <h5>{{ jb.title }}</h5>
  </h4>
</template>

<script>
export default {

  name:'Jobs',

  data() {
    return {
      jobs: [
        {title:"web" , id:1 , details: "lorem" },
        {title:"design" , id:2 , details: "lorem" },
        {title: "UI", id:3 , details: "lorem"  }
     ]
   }
  }
  
}
</script>

 