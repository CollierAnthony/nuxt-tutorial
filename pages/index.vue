<template>
  <div>
    <h2>Welcome to the best corny dad jokes app on the web</h2>
  </div>
</template>

<script>
  import AppHeader from "~/components/AppHeader";
  export default {
    components: {AppHeader},
    head(){
      return {
        title: 'Welcome to dad jokes',
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
