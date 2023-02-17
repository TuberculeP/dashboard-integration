<template>
  <div class="nav">
    <div id="bell">
      <svg width="37" height="42" viewBox="0 0 37 42" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M26.375 29.3184V30.3679L27.1241 31.1029L28.9447 32.8892H4.05527L5.87585 31.1029L6.625 30.3679V29.3184V19.2005C6.625 13.8744 9.41719 9.90539 13.9723 8.84649L15.9062 8.39692V6.41142V5.03538C15.9062 4.78119 16.1237 4.5 16.5 4.5C16.8763 4.5 17.0938 4.78119 17.0938 5.03538V6.41142V8.39535L19.0258 8.84605C23.5637 9.90464 26.375 13.8968 26.375 19.2005V29.3184Z" stroke="url(#paint0_linear_1_6)" stroke-width="5"/>
        <path d="M21 37C21 38.3261 20.5259 39.5979 19.682 40.5355C18.8381 41.4732 17.6935 42 16.5 42C15.3065 42 14.1619 41.4732 13.318 40.5355C12.4741 39.5979 12 38.3261 12 37L16.5 37H21Z" fill="url(#paint1_linear_1_6)"/>
        <defs>
          <linearGradient id="paint0_linear_1_6" x1="16.5" y1="2" x2="16.5" y2="41.4599" gradientUnits="userSpaceOnUse">
            <stop stop-color="#3254BD" offset="0"/>
            <stop offset="0.839229" stop-color="#6C1182"/>
            <stop offset="1" stop-color="#4E33A0"/>
          </linearGradient>
          <linearGradient id="paint1_linear_1_6" x1="16" y1="37" x2="16" y2="42" gradientUnits="userSpaceOnUse">
            <stop stop-color="#312FAF" offset="0"/>
            <stop offset="0.416577" stop-color="#552C9A"/>
            <stop offset="0.9375" stop-color="#6C1283"/>
          </linearGradient>
        </defs>
      </svg>
    </div>
    <img src="@/assets/profile.jpeg" alt="profile" id="profile" draggable="false">
  </div>
</template>

<script>
export default {
  name: "RightbarNav"
}
</script>

<style scoped lang="scss">
div.nav{
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 15px;
  #bell{
    position: relative;
    width: 33px;
    height: 41px;
    fill: none;
    &::after{
      content: "";
      position: absolute;
      display: block;
      top: -5px;
      right: -5px;
      width: 10px;
      height: 10px;
      border-radius: 50%;
      background-color: #6C1182;
    }
  }
  img{
    display: block;
    &#profile{
      width: 50px;
      aspect-ratio: 1/1;
      border-radius: 50%;
      object-fit: cover;
    }
    &:hover{
      cursor: pointer;
    }
  }
}
</style>