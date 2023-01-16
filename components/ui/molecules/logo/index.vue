<template>
  <div v-bind=logoAttr>
    <NuxtLink :to=logoLink v-if="logoLink">
      <A_Img 
        :imgAttr=imgAttr
        :imgSources=imgSources
        :imgClick=logoClick
      />
    </NuxtLink>
    <A_Img 
      v-else
      :imgAttr=imgAttr
      :imgSources=imgSources
      :imgClick=logoClick
    />
  </div>
</template>
<script>
  import A_Img from '~/components/ui/atoms/img/A_Img'
  export default {
    name: "M_Logo",
    data() {
      return {}
    },
    components: { A_Img },
    props: {
      logoLink: {
        type: String,
        default: ''
      },
      logoAttr: {
        type: Object,
        default: {}
      },
      logoClick: {
        type: Function,
        default: ()=>{}
      },
      ...A_Img.props
    },
  }
</script>