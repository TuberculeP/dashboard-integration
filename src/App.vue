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
  mounted() {
    const burger_left = document.querySelector(".burger.left");
    const burger_right = document.querySelector(".burger.right");
    const sidebar = document.querySelector(".sidebar");
    const rightbar = document.querySelector(".rightbar");
    const close_buttons = document.querySelectorAll(".close");
    const main = document.querySelector(".main");

    burger_left.addEventListener("click", () => {
      sidebar.classList.toggle("active");
      main.style.display = "none";

    });
    burger_right.addEventListener("click", () => {
      rightbar.classList.toggle("active");
      main.style.display = "none";

    });
    close_buttons.forEach((close_button) => {
      close_button.addEventListener("click", () => {
        sidebar.classList.remove("active");
        rightbar.classList.remove("active");
        main.style.display = "block";
      });
    });
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

@media screen and (max-width: 768px){
  .main-container{
    >div{
      padding: 0;
    }
    display: block;
    >div.sidebar{
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      z-index: 100;
    }
    >div.rightbar{
      display: none;
      position: fixed;
      top: 0;
      right: 0;
      width: 100%;
      z-index: 100;
    }
    >div.sidebar.active, >div.rightbar.active{
      display: block;
      background-color: black;
    }
    >div.main{
      position: relative;
      z-index: 0;
    }
  }
}
</style>
