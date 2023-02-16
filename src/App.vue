<template>
  <div class="main-container">
    <SidebarComponent/>
    <MainComponent/>
    <RightbarComponent/>
  </div>
</template>

<script>
import SidebarComponent from './components/SidebarComponent.vue'
import RightbarComponent from './components/RightbarComponent.vue'
import MainComponent from './components/MainComponent.vue'

export default {
  name: 'App',
  components: {
    SidebarComponent, RightbarComponent, MainComponent
  },
  data() {
    return {
    }
  },
  methods: {
  },
  mounted() {
  }
}
</script>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Poppins', sans-serif;
}
:root{
  font-size: 15px;
}
body{
  background-color: black;
  color: white;
}

.main-container{
  display: grid;
  grid-template-columns: 2fr 5fr 3fr;
  >div{
    //border: 1px solid white;
    padding: 1rem;
    position: relative;
    height: 100vh;
    overflow: scroll;
    &::-webkit-scrollbar{
      width: 0;
    }
    -ms-overflow-style: none;
    scrollbar-width: none;
  }
}
</style>
