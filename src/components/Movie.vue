<template>
  <main>
    <ul>
      <img :src="info.poster_path" :alt="info.title">
      <li>
        {{ info.title }}
      </li>
    </ul>
  </main>
</template>

<script>

export default {
  name: 'Movie',
  props: ['info']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
