
<template>
    <h2>Job Desc</h2>
    <p>{{ id }}</p>
</template>

<script>

export default {

  data() {
    return {
      id: this.$route.params.id 
    }
  }

}

</script>
 
