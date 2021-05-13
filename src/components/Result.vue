<template>
  <p>Reaction time - {{ score }} ms</p>
  <p v-if="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ['score'],
  data () {
    return {
      rank: null
    }
  },
  mounted () {
    if (this.score < 250) {
      this.rank = 'High level rank'
    } else if (this.score < 500) {
      this.rank = 'Nomal level rank'
    } else {
      this.rank = 'Low level rank'
    }
  }
}
</script>
