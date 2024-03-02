<script setup>

useHead({
  link:[
    {
      rel:'stylesheet',
      href:'https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.2/css/bootstrap.min.css'
    },
    {
      rel:'stylesheet',
      href:'https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css'
    }
  ],
  script:{
    src:'https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.2/js/bootstrap.min.js'
  }
});

</script>


<template>

  <NuxtLayout>
    <NuxtPage/>
  </NuxtLayout>

</template>