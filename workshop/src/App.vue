<template>
<div>
    <Header/>
    <router-view></router-view>
</div>
</template>

<script>

import Header from './components/Header'
  export default {
    components:
    {
      Header    
    }
  }
</script>