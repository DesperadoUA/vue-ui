<template>
  <div>
    <O_Header/>
    <main>
      <Nuxt />
    </main>
    <O_Footer />
  </div>
</template>
<script>
import O_Header from '~/components/header/'
import O_Footer from '~/components/footer/'
export default {
  name: 'mainLayout',
  components: {O_Header, O_Footer}
}
</script>
<style>
  * {
    padding: 0px;
    margin: 0px;
  }
  .d-inline {
    display: inline;
  }
  .d-flex {
    display: flex;
  }
  .br {
    border: 1px solid red;
  }
  img {
    display: block;
  }
  .border-radius-8 {
    border-radius: 8px;
  }
  .container {
    width: 1270px;
    max-width: 90%;
    margin: 0 auto;
  }
  .wrapper {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
  }
</style>