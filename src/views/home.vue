<template>
<div class="home">
  <Card/>
  <Card :isLoading="true"/>
</div>
</template>

<script>
import Card from '../components/card.vue'
export default {
  components: {
    Card
  },
  setup () {
    return {

    }
  }
}
</script>

<style lang="scss" scoped>
.home{
  background-color: #eee;
  min-height: 100vh;
  display: grid;
  grid-template-columns: 1fr;
  @media (min-width: 600px) {
    grid-template-columns: repeat(2, 1fr);
  }
}
</style>