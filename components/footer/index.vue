<template>
    <footer>
      <div class="container d-flex">
        <M_Logo 
          :imgAttr=logoSetting.imgAttr
          :imgSources=logoSetting.imgSources
          :logoAttr=logoSetting.logoAttr
          :logoLink=logoSetting.logoLink
          :logoClick=logoClick
        />
      </div>
    </footer>
  </template>
  <script>
    import M_Logo from '~/components/ui/molecules/logo/'
    export default {
      name: "O_footer",
      data() {
        return {
          logoSetting: {
            imgAttr: {
              src: '/ui/logo-2.png',
              alt: 'Custom Alt',
              title: 'Custom title',
              class: 'Custom class border-radius-8'
            },
            imgSources: [
             { media: "(max-width:650px)", srcset: '/ui/logo.jpg' }
            ],
            logoLink: '/',
            logoAttr: {
              class: 'customLogoClass br border-radius-8'
            },
          }
        }
      },
      components: {M_Logo},
      methods: {
        logoClick() {
          console.log('Logo click footer')
        }
      }
    }
  </script>
  <style>
   
  </style>