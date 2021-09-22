<template>
  <Aristidebenoist
    :items="items"
    :itemsWidth="700"
    :itemsHeight="400"
    :defaultBackgroundColor="'white'"
  />
</template>

<script>
import { Aristidebenoist } from 'didof-common'
import pics from './assets/pics.json'

export default {
  name: 'App',
  components: {
    Aristidebenoist,
  },
  setup() {
    const items = pics.map((pic, index) => ({
      ...pic,
      key: index,
      src: require(`@/assets/${pic.src}`),
    }))

    return { items }
  },
}
</script>

<style>
body {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  overflow: hidden;
}
</style>
