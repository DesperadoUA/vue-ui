<template>
  <picture>
    <source v-for="(source, index) in imgSources"
      :key=index
      :media=source.media
      :srcset=source.srcset
    >
    <img v-bind=imgAttr @click=imgClick />
  </picture>
</template>
<script>
  export default {
    name: "A_Img",
    data() {
      return {}
    },
    props: {
      imgAttr: {
        type: Object,
        default: {
          src: '/ui/logo.jpg',
          title: 'Title img',
          alt: 'Alt Img'
        }
      },
      imgSources: {
        type: Array,
        default: [
          /*{
              media: "(min-width:650px)",
              srcset: '/img/logo.jpg'
            },*/
          ],
      },
      imgClick: {
        type: Function,
        default: ()=>{}
      }
    },
  }
</script>