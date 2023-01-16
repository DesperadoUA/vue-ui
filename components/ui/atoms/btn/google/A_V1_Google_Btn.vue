<template>
   <button 
    :class="getType(googleBtnType)" 
    v-bind=googleBtnAttr
   >
    <span class="iconContainer">
      <img :src=googleBtnIcon class="icon" />
    </span>
    {{googleBtnText}}
   </button>
</template>
<script>
import  ModificationListMixin from '~/components/ui/mixin/modificationList'
    export default {
      name: "A_V1_Google_Btn",
      mixins: [ModificationListMixin],
      data() {
        return {}
      },
      props: {
        googleBtnAttr: {
          type: Object,
          default() {
            return {}
          }
        },
        googleBtnText: {
          type: String,
          default: 'Sign in with Google'
        },
        googleBtnClick: {
          type: Function,
          default: ()=>{}
        },
        googleBtnType: {
          type: String,
          default: 'default'
        },
        googleBtnIcon: {
          type: String,
          default: '/ui/google/google.svg'
        }
      },
      methods: {
        getType(type) {
            return this.modificationList.has(type)
             ? type
             : this.googleBtnType
        }
      }
    }
</script>
<style scope>
    button {
        display: flex;
        border: none;
        align-items: center;
        cursor: pointer;
        text-align: center;
        position: relative;
        min-height: 45px;
    }
    button.primary {
        background: var(--color-primary);
    }
    button.warning {
        background: var(--color-warning);
    }
    button.default {
        background: var(--color-default);
    }
    button.danger {
        background: var(--color-danger);
        color: var(--color-white);
    }
    button.success {
        background: var(--color-success);
    }
    button.inverse {
        background: var(--color-inverse);
    }
    button.info {
        background: var(--color-info);
    }
    button.disabled {
        background: var(--color-disabled);
    }
    .icon {
       max-width: 100%;
    }
    .iconContainer {
      display: flex;
      height: 100%;
      min-width: 40px;
      align-items: center;
      justify-content: center;
    }
    button:has(.icon) {
        padding-right: var(--gap-md);
    }
</style>