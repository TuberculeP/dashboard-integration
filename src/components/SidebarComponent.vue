<template>
  <div class="sidebar">
    <div class="close">
      <div>
        <div class="line"></div>
        <div class="line"></div>
      </div>
    </div>
    <div id="logo">
      <img src="../assets/minance_logo.png" alt="logo" draggable="false">
      <h1>inance</h1>
    </div>
    <div class="content">
      <SidebarButton/>
      <nav>
        <ul>
          <SidebarLI
              icon='<svg width="39" height="39" viewBox="0 0 39 39" fill="none" xmlns="http://www.w3.org/2000/svg">
<path opacity="0.8" d="M17.3889 38.5H4.72222C2.4 38.5 0.5 36.6 0.5 34.2778V4.72222C0.5 2.4 2.4 0.5 4.72222 0.5H17.3889V38.5ZM21.6111 38.5H34.2778C36.6 38.5 38.5 36.6 38.5 34.2778V19.5H21.6111V38.5ZM38.5 15.2778V4.72222C38.5 2.4 36.6 0.5 34.2778 0.5H21.6111V15.2778H38.5Z"/>
</svg>'
              text="Invoices"/>
          <SidebarLI
            icon='<svg width="56" height="38" viewBox="0 0 56 38" fill="none" xmlns="http://www.w3.org/2000/svg">
<path opacity="0.8" d="M38 16.2857C42.15 16.2857 45.475 12.6486 45.475 8.14286C45.475 3.63714 42.15 0 38 0C33.85 0 30.5 3.63714 30.5 8.14286C30.5 12.6486 33.85 16.2857 38 16.2857ZM18 16.2857C22.15 16.2857 25.475 12.6486 25.475 8.14286C25.475 3.63714 22.15 0 18 0C13.85 0 10.5 3.63714 10.5 8.14286C10.5 12.6486 13.85 16.2857 18 16.2857ZM18 21.7143C12.175 21.7143 0.5 24.89 0.5 31.2143V38H35.5V31.2143C35.5 24.89 23.825 21.7143 18 21.7143ZM38 21.7143C37.275 21.7143 36.45 21.7686 35.575 21.85C38.475 24.13 40.5 27.1971 40.5 31.2143V38H55.5V31.2143C55.5 24.89 43.825 21.7143 38 21.7143Z"/>
</svg>'
            text="Clients"/>
          <SidebarLI
            icon='<svg width="45" height="43" viewBox="0 0 45 43" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M42.7992 3.58022C43.0709 3.53215 43.35 3.58667 43.5869 3.73408C43.7982 3.82792 43.9786 3.98455 44.1058 4.18463C44.2331 4.38471 44.3017 4.61947 44.3031 4.85994L44.5072 34.4435C44.5189 34.6677 44.4721 34.891 44.3718 35.0894C44.2715 35.2878 44.1214 35.4537 43.9378 35.5694L32.4115 42.7561C32.2047 42.9173 31.9531 43.003 31.6953 43C31.6322 43.0057 31.5687 43.0057 31.5055 43L1.61362 39.4986C1.31465 39.4824 1.03288 39.3471 0.825898 39.1204C0.618918 38.8937 0.502349 38.5927 0.500012 38.2789V8.17369C0.495738 7.92813 0.561649 7.68685 0.689269 7.48086C0.81689 7.27488 1.00039 7.11362 1.21616 7.01782L16.2158 0.101339C16.4103 0.00696927 16.6262 -0.0281441 16.8389 1.25095e-05L42.7992 3.56896V3.58022ZM29.4574 4.2182L20.6237 9.47217L31.502 10.9283L39.5586 5.60675L29.4574 4.2182ZM19.0733 11.7239L18.6722 24.2508L14.1891 21.0497L9.70965 23.7067L10.6156 10.6055L2.84539 9.56599V37.1719L30.5352 40.3993V13.27L19.0768 11.7351L19.0733 11.7239ZM12.0192 8.31255L20.5951 3.00228L16.8639 2.48439L5.95704 7.50569L12.0264 8.32005L12.0192 8.31255ZM32.8841 12.9135V39.6037L42.1582 33.8093L41.972 6.90899L32.8841 12.9135Z"/>
</svg>
'
            text="Products"/>
          <SidebarLI
            icon='<svg width="41" height="33" viewBox="0 0 41 33" fill="none" xmlns="http://www.w3.org/2000/svg">
<path opacity="0.8" d="M4.5 0H36.5C38.7 0 40.48 1.85625 40.48 4.125L40.5 28.875C40.5 31.1437 38.7 33 36.5 33H4.5C2.3 33 0.5 31.1437 0.5 28.875V4.125C0.5 1.85625 2.3 0 4.5 0ZM4.5 8.25L20.5 18.5625L36.5 8.25V4.125L20.5 14.4375L4.5 4.125V8.25Z"/>
</svg>
'
            text="Messages"/>
          <SidebarLI
            icon='<svg width="40" height="42" viewBox="0 0 40 42" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M35.035 22.9975C35.12 22.36 35.1625 21.7012 35.1625 21C35.1625 20.32 35.12 19.64 35.0137 19.0025L39.3275 15.645C39.71 15.3475 39.8162 14.7737 39.5825 14.3487L35.5025 7.29373C35.2475 6.82623 34.7162 6.67747 34.2487 6.82622L29.17 8.86622C28.1075 8.05872 26.9812 7.37872 25.7275 6.86872L24.9625 1.47123C24.8775 0.961225 24.4525 0.599976 23.9425 0.599976H15.7825C15.2725 0.599976 14.8687 0.961225 14.7837 1.47123L14.0187 6.86872C12.765 7.37872 11.6175 8.07997 10.5762 8.86622L5.49748 6.82622C5.02998 6.65622 4.49873 6.82623 4.24373 7.29373L0.184977 14.3487C-0.0700232 14.795 0.0149766 15.3475 0.439977 15.645L4.75373 19.0025C4.64748 19.64 4.56248 20.3412 4.56248 21C4.56248 21.6587 4.60498 22.36 4.71123 22.9975L0.397477 26.355C0.0149766 26.6525 -0.0912732 27.2262 0.142477 27.6512L4.22248 34.7062C4.47748 35.1737 5.00873 35.3225 5.47623 35.1737L10.555 33.1337C11.6175 33.9412 12.7437 34.6212 13.9975 35.1312L14.7625 40.5287C14.8687 41.0387 15.2725 41.4 15.7825 41.4H23.9425C24.4525 41.4 24.8775 41.0387 24.9412 40.5287L25.7062 35.1312C26.96 34.6212 28.1075 33.9412 29.1487 33.1337L34.2275 35.1737C34.695 35.3437 35.2262 35.1737 35.4812 34.7062L39.5612 27.6512C39.8162 27.1837 39.71 26.6525 39.3062 26.355L35.035 22.9975ZM19.8625 28.65C15.655 28.65 12.2125 25.2075 12.2125 21C12.2125 16.7925 15.655 13.35 19.8625 13.35C24.07 13.35 27.5125 16.7925 27.5125 21C27.5125 25.2075 24.07 28.65 19.8625 28.65Z"/>
</svg>
'
            text="Settings"/>
          <SidebarLI
            icon='<svg width="49" height="47" viewBox="0 0 49 47" fill="none" xmlns="http://www.w3.org/2000/svg">
<path opacity="0.8" d="M24.5 0C11.252 0 0.5 10.528 0.5 23.5C0.5 36.472 11.252 47 24.5 47C37.748 47 48.5 36.472 48.5 23.5C48.5 10.528 37.748 0 24.5 0ZM26.9 39.95H22.1V35.25H26.9V39.95ZM31.868 21.7375L29.708 23.8995C27.98 25.615 26.9 27.025 26.9 30.55H22.1V29.375C22.1 26.79 23.18 24.44 24.908 22.7245L27.884 19.7635C28.772 18.9175 29.3 17.7425 29.3 16.45C29.3 13.865 27.14 11.75 24.5 11.75C21.86 11.75 19.7 13.865 19.7 16.45H14.9C14.9 11.2565 19.196 7.05 24.5 7.05C29.804 7.05 34.1 11.2565 34.1 16.45C34.1 18.518 33.236 20.398 31.868 21.7375Z"/>
</svg>
'
            text="Help"/>

        </ul>
      </nav>
    </div>
    <div class="logout">
      <svg width="40" height="35" viewBox="0 0 40 35" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M30 7.77778L27.18 10.5194L32.34 15.5556H12V19.4444H32.34L27.18 24.4611L30 27.2222L40 17.5L30 7.77778ZM4 3.88889H20V0H4C1.8 0 0 1.75 0 3.88889V31.1111C0 33.25 1.8 35 4 35H20V31.1111H4V3.88889Z"/>
      </svg>
      <p>Log Out</p>
    </div>
  </div>

</template>

<script>
import SidebarButton from './Sidebar/SidebarButton.vue'
import SidebarLI from './Sidebar/SidebarLI.vue'

export default {
  name: "SidebarComponent",
  components: {
    SidebarButton, SidebarLI
  },
}
</script>

<style scoped lang="scss">
div.sidebar{

}
div#logo{
  display: flex;
  justify-content: left;
  align-items: flex-end;
  user-select: none;
  padding: 15px;
  margin-bottom: 45px;
  img{
    height: 40px;
  }
  h1{
    line-height: 1.5rem;
  }
}
div.content{
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 50px;
}

div.logout{
  position: absolute;
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 10px;
  padding: 15px;
  margin: 15px auto;
  border-radius: 17px;
  width: 80%;
  svg{
    width: 2rem;
    height: 2rem;
    fill: white;
  }
  &:hover{
    cursor: pointer;
    background-color: darkred;
    svg{
      fill: black;
    }
    p{
      color: black;
    }
  }
}
div.close{
  display: none;
}
@media screen and (max-width: 768px){
  div#logo{
    justify-content: center;
  }
  div.close{
    display: flex;
    justify-content: flex-start;
    position: absolute;
    top: 20px;
    left: 10px;
    div{
      position: relative;
      cursor: pointer;
      width: 30px;
      height: 30px;
      .line{
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        width: 100%;
        height: 2px;
        background: white;
        transition: all 0.3s ease;
        &:first-child{
          transform: rotate(45deg);
        }
        &:last-child{
          transform: rotate(-45deg);
        }
      }
    }
  }
}
</style>