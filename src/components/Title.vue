<template>
  <div class="title-class">
    <h1>{{ message }}</h1>
  </div>
</template>

<script>
  export default {
    name: 'Title',
    props: {
      message: String
    }
  }
  
</script>
