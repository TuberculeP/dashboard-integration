<template>
  <div class="transaction">
    <div class="icon" v-html="icons[currency]"></div>
    <div class="currency">
      <h5>{{currency}}</h5>
      <p>{{names[currency]}}</p>
    </div>
    <div class="market-cap">
      <h5>Market Cap</h5>
      <p>${{MarketCap}}</p>
    </div>
    <div class="day-change">
      <h5>Day Change</h5>
      <p>{{DayChange}}</p>
    </div>
    <div class="merdouille">
      <svg width="151" height="18" viewBox="0 0 151 18" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M4 7.04242C6.73136 9.3383 14.7845 12.5525 25.146 7.04242C35.5076 1.53231 42.151 4.74654 44.1774 7.04242C46.4683 10.3223 52.8473 15.898 60.037 11.9622C69.024 7.04242 74.3105 2.12267 86.4695 7.04242C98.6285 11.9622 108.408 16.8819 112.902 11.9622C117.396 7.04242 142.506 2.12267 147 7.04242" stroke="url(#paint0_linear_16_119)" stroke-width="7" stroke-linecap="round"/>
        <defs>
          <linearGradient id="paint0_linear_16_119" x1="75.5" y1="14" x2="75.5" y2="4" gradientUnits="userSpaceOnUse">
            <stop :stop-color="bottom_gradient[currency]" offset="0"/>
            <stop offset="1" stop-color="#4D91A5"/>
          </linearGradient>

        </defs>
      </svg>


    </div>
    <button>Trade</button>
  </div>
</template>

<script>
export default {
  name: "MainTransaction",
  props: {
    currency: String,
    MarketCap: String,
    DayChange: String,
  },
  data() {
    return {
      icons: {
        "BTC": '<svg width="40" height="40" viewBox="0 0 40 40" fill="none" xmlns="http://www.w3.org/2000/svg">\n' +
            '<path fill-rule="evenodd" clip-rule="evenodd" d="M18.334 20.5836L21.9069 21.5422C23.5744 21.9896 24.2689 23.3689 23.8038 24.9483C23.4953 26.1011 22.7025 26.9961 21.6434 27.138C21.2436 27.2011 20.7169 27.1024 20.2802 26.9852L16.866 26.0692L18.334 20.5836ZM24.7163 14.5418C25.3245 15.131 25.4691 16.0219 25.2244 16.9361C24.8415 18.3672 23.7418 19.1373 22.3127 18.7539L19.0573 17.8805L20.3444 13.0705L23.2028 13.8374C23.838 14.0078 24.3725 14.2366 24.7163 14.5418ZM19.8638 29.8133C19.3674 31.6684 19.1192 32.596 19.1192 32.596C19.1192 32.596 18.4972 32.4291 17.2533 32.0953L17.9979 29.3127L16.0527 28.7908C15.5562 30.6459 15.308 31.5734 15.308 31.5734C15.308 31.5734 14.6861 31.4066 13.4422 31.0728L14.1868 28.2901C11.6989 27.6226 10.455 27.2889 10.455 27.2889C10.455 27.2889 10.6819 26.4409 11.1358 24.745L12.2871 25.0539C12.8825 25.2136 13.4469 24.8537 13.5958 24.2972L16.6062 13.0476C16.7658 12.4513 16.4064 11.8863 15.8506 11.7372C15.0831 11.5312 14.6993 11.4283 14.6993 11.4283C14.6993 11.4283 14.9262 10.5802 15.3801 8.88412L19.1119 9.88537C19.6083 8.03031 19.8565 7.10277 19.8565 7.10277C19.8565 7.10277 20.4785 7.26964 21.7224 7.60338L20.9778 10.386L22.923 10.9079C23.4194 9.05282 23.6676 8.12529 23.6676 8.12529C23.6676 8.12529 24.2896 8.29217 25.5336 8.62592L24.7783 11.4482C25.7204 11.7436 26.4428 12.0653 27.112 12.5857C28.6092 13.669 29.3457 15.5282 28.7925 17.5953C28.3244 19.3444 27.1474 20.5624 25.4765 20.9235C27.36 22.1532 27.7944 24.1869 27.2732 26.1348C26.5634 28.6284 24.4066 30.0096 22.2514 30.1131C21.3937 30.1386 20.6578 30.0263 19.8638 29.8133ZM1.0528 14.8819C-1.7342 25.2967 4.4559 36.0326 14.8572 38.8232C25.2585 41.6139 35.9802 35.4155 38.7672 25.0007C41.5542 14.5858 35.364 3.85005 24.9628 1.0594C14.5615 -1.73128 3.83979 4.46705 1.0528 14.8819Z" fill="#F7931A"/>\n' +
            '</svg>\n',
        "ETH": '<svg width="41" height="39" viewBox="0 0 41 39" fill="none" xmlns="http://www.w3.org/2000/svg">\n' +
            '<ellipse cx="20.3283" cy="19.1153" rx="20.3283" ry="19.1153" fill="white"/>\n' +
            '<path fill-rule="evenodd" clip-rule="evenodd" d="M9.89661 19.1153L20.5957 3.01819V14.7811L9.89661 19.1153ZM30.7598 19.1153L20.5957 14.7868V3.01819L30.7598 19.1153Z" fill="#828384"/>\n' +
            '<path fill-rule="evenodd" clip-rule="evenodd" d="M20.5957 25.1516L9.89661 19.493L20.5957 15.0909V25.1516ZM30.7598 19.4939L20.5957 25.1516V15.0909L30.7598 19.4939Z" fill="#343535"/>\n' +
            '<path fill-rule="evenodd" clip-rule="evenodd" d="M9.89661 21.6305L20.5957 27.4381V35.2124L9.89661 21.6305ZM30.7598 21.6305L20.5957 35.2124V27.4374L30.7598 21.6305Z" fill="#828384"/>\n' +
            '<path fill-rule="evenodd" clip-rule="evenodd" d="M30.7598 19.1153L20.5957 14.7868V3.01819L30.7598 19.1153Z" fill="#2F3030"/>\n' +
            '<path fill-rule="evenodd" clip-rule="evenodd" d="M30.7598 19.4939L20.5957 15.0909V25.1516L30.7598 19.4939Z" fill="#131313"/>\n' +
            '<path fill-rule="evenodd" clip-rule="evenodd" d="M30.7598 21.6305L20.5957 27.4374V35.2124L30.7598 21.6305Z" fill="#2F3030"/>\n' +
            '</svg>\n',
      },
      colors: {
        "BTC": "#F7931A",
        "ETH": "#627EEA",
      },
      names: {
        "BTC": "Bitcoin",
        "ETH": "Ethereum",
      },
      bottom_gradient: {
        BTC: "#592795",
        ETH: "#091BA9"
    }
    }
  },
  created() {

  },
  mounted() {
    if(this.DayChange < 0) {
      this.$el.querySelector(".day-change p").classList.add("negative");
    }
    this.$el.querySelector(".market-cap p").style.color = this.colors[this.currency];
  },
}
</script>

<style scoped lang="scss">
div.transaction{
  >div{
    width: fit-content;
  }
  margin: 20px 20px;
  padding: 10px;
  background-color: rgba(32, 35, 43, 0.7);
  display: grid;
  grid-template-columns: repeat(5, 1fr) auto;
  align-items: center;
  border-radius: 1.5rem;
  svg{
    width:40px;
    height: 40px;
    display: block;
  }
  h5{
    font-size: 0.8rem;
    font-weight: normal
  }
  p{
    opacity: 0.8;
    &.negative{
      color: #FF4D4F;
    }
  }
  div.merdouille{
    svg{
      stroke: white;
      width: 70%;
    }
  }
  button{
    display: block;
    margin: 0;
    width: fit-content;
    padding: 5px 10px;
    border-radius: 50px;
    border: none;
    background-color: black;
    color: white;
    font-weight: 500;
  }
}
@media screen and (max-width: 768px){
  div.transaction{
    margin: 20px 0;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(2, 1fr);
    button{
      width: 100%;
    }
  }
}
</style>