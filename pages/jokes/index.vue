<template>
  <div>jokes</div>
</template>
<script>
  export default{
    data(){
      return{
        jokes : []
      }
    },
    head(){
      return {
        title: 'Dad Jokes',
        meta: [
          {
            hid: 'description',
            name: 'description',
            content: 'Best place for corny dad jokes'
          }
        ]
      }
    }
  };
</script>

<style></style>
