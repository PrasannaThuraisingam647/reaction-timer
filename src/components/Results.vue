<template>
  <h3 class="rank">{{rank}}</h3>
  <p>Reaction Time - {{score}} ms</p>
</template>

<script>
  export default {
    props: ['score'],
    data() {
      return {
        rank: null
      }
    },
    mounted() {
      if (this.score < 250) {
        this.rank = 'Ninja Fingers'
      } else if (this.score < 400) {
        this.rank = 'Rapid Reflexes'
      } else {
        this.rank = 'Snail Pace...'
      }
    }
  }
</script>

<style>
  .rank{
    color: #0faf87;
    font-weight: bold;
  }
</style>
