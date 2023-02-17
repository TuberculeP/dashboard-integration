<template>
  <div class="asset">
    <div class="icon" v-html="c_data[currency].icon"></div>
    <h3 class="currency">{{ c_data[currency].name }}</h3>
    <div class="value">
      <p>{{asset_value}}</p>
      <p>{{currency}}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "RightbarAsset",
  props: {
    currency: {
      type: String,
      required: true
    },
    asset_value: {
      type: String,
      required: true
    }
  },
  data() {
    return {
      c_data: {
        BTC: {
          gradient: "linear-gradient(98.73deg, #611D8D 35.75%, #2F7EC1 73.26%)",
          name: "Bitcoin",
          color: "white",
          icon: '<svg width="40" height="40" viewBox="0 0 40 40" fill="none" xmlns="http://www.w3.org/2000/svg">\n' +
              '<path fill-rule="evenodd" clip-rule="evenodd" d="M18.334 20.5836L21.9069 21.5422C23.5744 21.9896 24.2689 23.3689 23.8038 24.9483C23.4953 26.1011 22.7025 26.9961 21.6434 27.138C21.2436 27.2011 20.7169 27.1024 20.2802 26.9852L16.866 26.0692L18.334 20.5836ZM24.7163 14.5418C25.3245 15.131 25.4691 16.0219 25.2244 16.9361C24.8415 18.3672 23.7418 19.1373 22.3127 18.7539L19.0573 17.8805L20.3444 13.0705L23.2028 13.8374C23.838 14.0078 24.3725 14.2366 24.7163 14.5418ZM19.8638 29.8133C19.3674 31.6684 19.1192 32.596 19.1192 32.596C19.1192 32.596 18.4972 32.4291 17.2533 32.0953L17.9979 29.3127L16.0527 28.7908C15.5562 30.6459 15.308 31.5734 15.308 31.5734C15.308 31.5734 14.6861 31.4066 13.4422 31.0728L14.1868 28.2901C11.6989 27.6226 10.455 27.2889 10.455 27.2889C10.455 27.2889 10.6819 26.4409 11.1358 24.745L12.2871 25.0539C12.8825 25.2136 13.4469 24.8537 13.5958 24.2972L16.6062 13.0476C16.7658 12.4513 16.4064 11.8863 15.8506 11.7372C15.0831 11.5312 14.6993 11.4283 14.6993 11.4283C14.6993 11.4283 14.9262 10.5802 15.3801 8.88412L19.1119 9.88537C19.6083 8.03031 19.8565 7.10277 19.8565 7.10277C19.8565 7.10277 20.4785 7.26964 21.7224 7.60338L20.9778 10.386L22.923 10.9079C23.4194 9.05282 23.6676 8.12529 23.6676 8.12529C23.6676 8.12529 24.2896 8.29217 25.5336 8.62592L24.7783 11.4482C25.7204 11.7436 26.4428 12.0653 27.112 12.5857C28.6092 13.669 29.3457 15.5282 28.7925 17.5953C28.3244 19.3444 27.1474 20.5624 25.4765 20.9235C27.36 22.1532 27.7944 24.1869 27.2732 26.1348C26.5634 28.6284 24.4066 30.0096 22.2514 30.1131C21.3937 30.1386 20.6578 30.0263 19.8638 29.8133ZM1.0528 14.8819C-1.7342 25.2967 4.4559 36.0326 14.8572 38.8232C25.2585 41.6139 35.9802 35.4155 38.7672 25.0007C41.5542 14.5858 35.364 3.85005 24.9628 1.0594C14.5615 -1.73128 3.83979 4.46705 1.0528 14.8819Z" fill="white"/>\n' +
              '</svg>\n'
        },
        ETH: {
          gradient: "linear-gradient(99.56deg, #FAFF00 35.82%, #29ABE2 64.75%, rgba(255, 255, 255, 0.7) 91.33%)",
          name: "Ethereum",
          color: "black",
          icon: '<svg width="86" height="86" viewBox="0 0 86 86" fill="none" xmlns="http://www.w3.org/2000/svg">\n' +
              '<ellipse cx="42.91" cy="42.965" rx="42.91" ry="42.965" fill="black"/>\n' +
              '<path fill-rule="evenodd" clip-rule="evenodd" d="M20.8903 42.965L43.4745 6.78394V33.2232L20.8903 42.965ZM64.9295 42.965L43.4745 33.236V6.78394L64.9295 42.965Z" fill="#828384"/>\n' +
              '<path fill-rule="evenodd" clip-rule="evenodd" d="M43.4745 56.5327L20.8903 43.8139L43.4745 33.9196V56.5327ZM64.9295 43.8161L43.4745 56.5327V33.9196L64.9295 43.8161Z" fill="#343535"/>\n' +
              '<path fill-rule="evenodd" clip-rule="evenodd" d="M20.8903 48.6183L43.4745 61.672V79.1461L20.8903 48.6183ZM64.9295 48.6183L43.4745 79.1461V61.6705L64.9295 48.6183Z" fill="#828384"/>\n' +
              '<path fill-rule="evenodd" clip-rule="evenodd" d="M64.9294 42.965L43.4744 33.236V6.78394L64.9294 42.965Z" fill="white" fill-opacity="0.7"/>\n' +
              '<path fill-rule="evenodd" clip-rule="evenodd" d="M64.9294 43.8161L43.4744 33.9196V56.5327L64.9294 43.8161Z" fill="#131313"/>\n' +
              '<path fill-rule="evenodd" clip-rule="evenodd" d="M64.9294 48.6183L43.4744 61.6705V79.1461L64.9294 48.6183Z" fill="white" fill-opacity="0.7"/>\n' +
              '</svg>\n'
        }
      }

    }
  },
  mounted() {
    this.$el.style.background = this.c_data[this.currency].gradient;
    this.$el.style.color = this.c_data[this.currency].color;
  }
}
</script>

<style lang="scss">
div.asset{
  padding: 10px 20px;
  margin: 20px 10px;
  border-radius: 1.5rem;
  h3{
    font-weight: 500;
    font-size: 1rem;
  }
  .value{
    display: flex;
    justify-content: space-between;
    font-size: 1.5rem;
    margin-right: 50px;
  }
  .icon{
    svg{
      display: block;
      width: 50px;
      height: 50px;
    }
  }
}
</style>