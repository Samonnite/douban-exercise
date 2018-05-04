<template>
  <div class="pages-view">
    <header-bar @showTalion="open"></header-bar>
    <router-view></router-view>
    <talion-view v-show="talion" @closeTalion="close"></talion-view>
  </div>
</template>
<script>
  import HeaderBar from '../components/headerBar'
  import TalionView from '../views/talionView'
  export  default {
    name: 'pages-view',
    components: {
      HeaderBar,
      TalionView
    },
    data () {
      return {
        talion: ''
      }
    },
    methods: {
      open: function () {
        this.talion = 'open'
      },
      close: function () {
        this.talion = ''
      }
    }
  }
</script>
