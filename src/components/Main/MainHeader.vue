<template>
  <header>
    <h2>Hi, TuberPoirot</h2>
    <div class="search">
      <svg width="35" height="34" viewBox="0 0 35 34" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M29.9566 26.3967C30.6547 25.2949 31.0673 24.02 31.0673 22.6349C31.0673 18.7157 27.8781 15.5519 23.9272 15.5519C19.9764 15.5519 16.7871 18.7157 16.7871 22.6349C16.7871 26.5541 19.9764 29.7178 23.9113 29.7178C25.3076 29.7178 26.6087 29.3086 27.7035 28.6161L32.654 33.5269L34.9071 31.2918L29.9566 26.3967ZM23.9272 26.5699C21.7376 26.5699 19.9605 24.807 19.9605 22.6349C19.9605 20.4628 21.7376 18.6999 23.9272 18.6999C26.1168 18.6999 27.8939 20.4628 27.8939 22.6349C27.8939 24.807 26.1168 26.5699 23.9272 26.5699ZM23.356 13.1909C22.1819 13.2224 21.0553 13.4743 20.024 13.8992L19.1513 12.5928L13.1219 22.3201L8.34596 16.7796L2.5863 25.9245L0 24.083L7.93342 11.491L12.6935 17L19.0402 6.76906L23.356 13.1909ZM27.4655 13.9779C26.45 13.5372 25.3552 13.2696 24.2128 13.2067L32.3366 0.473091L34.9071 2.3304L27.4655 13.9779Z" fill="black"/>
      </svg>
      <input type="text" placeholder="Search">
    </div>
  </header>
</template>

<script>
export default {
  name: "MainHeader"
}
</script>

<style scoped lang="scss">
header{
  display: flex;
  justify-content: space-between;align-items: center;
  margin-right: 50px;
  background-color: black;
  h2{
    font-weight: normal;
  }
  div.search{
    background-color: white;
    border-radius: 15px;
    display: flex;
    align-items: center;
    padding: 0 15px;
    overflow: clip;
    width: 50%;
    input{
      border: none;
      outline: none;
      padding: 10px;
      font-size: 1rem;
      width: 100%;
    }
  }
}
@media screen and (max-width: 768px){
  header{
    display: block;
    margin: 0;
    h2{
      margin: 1rem 0;
      text-align: center;
    }
    div.search{
      margin: 1rem auto;
    }
  }
}
</style>