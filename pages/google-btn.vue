<template>
    <div class="container">
      <h1>Google Btn</h1>
      <hr>
      <div class="section wrapper">
        <div class="containerBtn" v-for="item in modificationList" :key="item"> 
        <A_V1_Google_Btn
          :googleBtnType=item 
        />
        </div>
      </div>
    </div>
  </template>
  
  <script>
  import A_V1_Google_Btn from '~/components/ui/atoms/btn/google/A_V1_Google_Btn'
  import  ModificationListMixin from '~/components/ui/mixin/modificationList'
  
  export default {
    name: 'GoogleBtn',
    layout: 'main',
    mixins: [ModificationListMixin],
    components: { A_V1_Google_Btn }
  }
  </script>
<style>
    .section {
        padding-top: var(--gap-lg);
        padding-bottom: var(--gap-lg);
    }
    .containerBtn {
        padding: var(--gap-sm);
    }
</style>
  