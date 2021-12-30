<template>
  <div class="single-logo">
      <img :src="logo.path" alt="logo.alt" />
  </div>
</template>

<script>
export default {
    props: ['logo'],
    
}
</script>

<style scoped lang="scss">
    .single-logo {
        // border: 1px solid white;
        // width: 130px;
        height: 80px;
        max-width: 40%;
        display: flex;
        align-items: center;
        justify-content: center;
        margin: 2em 3em;

        img {
            width: 100%;
            height: 100%;
        }
    }
</style>