<template>
<div class="transaction">
  <div class="icon" v-html="c_data[currency].icon"></div>
  <div class="type">
    <h3>{{c_data[currency].name}}</h3>
    <p>{{transactions[transaction_type]}}</p>
  </div>
  <div class="value">
    <p class="value">{{ value }}</p>
    <p class="date">{{date}}</p>
  </div>
</div>
</template>

<script>
export default {
  name: "RightbarTransactions",
  props: {
    currency: {
      type: String,
      required: true
    },
    transaction_type: {
      type: String,
      required: true
    },
    transaction_value: {
      type: String,
      required: true
    },
    date: {
      type: String,
      required: true
    }
  },
  computed: {
    value(){
      return this.transaction_value>0?`+${this.transaction_value}`:this.transaction_value
    }
  },
  mounted() {
    if(this.value>0) {
      this.$el.classList.add('negative')
    }
  },
  data() {
    return {
      c_data: {
        BTC: {
          name: 'Bitcoin',
          icon: '<svg width="52" height="52" viewBox="0 0 52 52" fill="none" xmlns="http://www.w3.org/2000/svg">\n' +
              '<g filter="url(#filter0_i_16_276)">\n' +
              '<path d="M26 52C40.3594 52 52 40.3594 52 26C52 11.6406 40.3594 0 26 0C11.6406 0 0 11.6406 0 26C0 40.3594 11.6406 52 26 52Z" fill="#FF8E04"/>\n' +
              '<path d="M37.6821 22.7825C38.1924 19.3765 35.5973 17.5451 32.0515 16.3231L33.202 11.7081L30.394 11.0094L29.2728 15.5025C28.535 15.3173 27.7778 15.145 27.0221 14.9728L28.1515 10.4504L25.3435 9.75L24.193 14.3634C23.582 14.2236 22.9808 14.0871 22.399 13.9409L22.4023 13.9262L18.5283 12.9594L17.7808 15.9591C17.7808 15.9591 19.8656 16.4369 19.8218 16.4661C20.9593 16.7505 21.164 17.5029 21.1299 18.1009L19.8201 23.3577C19.8981 23.3773 19.9989 23.4065 20.1126 23.4504L19.8153 23.3773L17.979 30.7418C17.8393 31.0863 17.4866 31.6046 16.6904 31.408C16.7196 31.4486 14.6494 30.8994 14.6494 30.8994L13.2551 34.1136L16.9114 35.0253C17.5906 35.1959 18.2569 35.3746 18.9118 35.542L17.7499 40.209L20.5563 40.9078L21.7068 36.2928C22.4738 36.4991 23.218 36.6909 23.946 36.8729L22.7988 41.4684L25.6068 42.1671L26.7686 37.5099C31.5591 38.4166 35.1601 38.051 36.6763 33.7188C37.8983 30.2315 36.6161 28.2181 34.0958 26.9068C35.932 26.4843 37.3132 25.2769 37.6821 22.7825ZM31.2634 31.7818C30.3973 35.2706 24.5229 33.384 22.6184 32.9111L24.1621 26.728C26.0666 27.2041 32.1718 28.145 31.2634 31.7818ZM32.1328 22.7321C31.3414 25.9058 26.4534 24.2921 24.869 23.8973L26.2665 18.291C27.8509 18.6859 32.9583 19.422 32.1328 22.7321Z" fill="white"/>\n' +
              '</g>\n' +
              '<defs>\n' +
              '<filter id="filter0_i_16_276" x="0" y="0" width="55" height="55" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">\n' +
              '<feFlood flood-opacity="0" result="BackgroundImageFix"/>\n' +
              '<feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape"/>\n' +
              '<feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha"/>\n' +
              '<feOffset dx="12" dy="4"/>\n' +
              '<feGaussianBlur stdDeviation="1.5"/>\n' +
              '<feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1"/>\n' +
              '<feColorMatrix type="matrix" values="0 0 0 0 1 0 0 0 0 0.555053 0 0 0 0 0.0166667 0 0 0 1 0"/>\n' +
              '<feBlend mode="normal" in2="shape" result="effect1_innerShadow_16_276"/>\n' +
              '</filter>\n' +
              '</defs>\n' +
              '</svg>\n'
        },
        USDT: {
          name: "Usdt",
          icon: '<svg width="54" height="54" viewBox="0 0 54 54" fill="none" xmlns="http://www.w3.org/2000/svg">\n' +
              '<g filter="url(#filter0_b_16_214)">\n' +
              '<path fill-rule="evenodd" clip-rule="evenodd" d="M27 0C41.911 0 54 12.089 54 27C54 41.911 41.9105 54 27 54C12.0895 54 0 41.9143 0 27C0 12.0857 12.0874 0 27 0Z" fill="#18624D"/>\n' +
              '</g>\n' +
              '<g filter="url(#filter1_b_16_214)">\n' +
              '<path fill-rule="evenodd" clip-rule="evenodd" d="M30.3345 29.4959V29.4927C30.1471 29.5045 29.1843 29.5623 27.0405 29.5623C25.3265 29.5623 24.1207 29.5137 23.6957 29.4916V29.497C17.1002 29.2048 12.177 28.0563 12.177 26.682C12.177 25.3077 17.1007 24.1607 23.6957 23.868V28.3527C24.1277 28.3824 25.3633 28.4553 27.0686 28.4553C29.1168 28.4553 30.1466 28.37 30.3356 28.3527V23.868C36.9182 24.1612 41.83 25.3109 41.83 26.6803C41.83 28.0498 36.916 29.2 30.3356 29.4932M30.3323 23.4025V19.386H39.5172V13.2662H14.5066V19.386H23.6925V23.3993C16.227 23.7422 10.6137 25.2207 10.6137 26.9919C10.6137 28.7631 16.2297 30.2416 23.6925 30.5867V43.4522H30.3345V30.5856C37.7865 30.2416 43.3885 28.7642 43.3885 26.9946C43.3885 25.225 37.7865 23.7476 30.3345 23.4036" fill="#F3E2E2"/>\n' +
              '</g>\n' +
              '<defs>\n' +
              '<filter id="filter0_b_16_214" x="-4" y="-4" width="62" height="62" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">\n' +
              '<feFlood flood-opacity="0" result="BackgroundImageFix"/>\n' +
              '<feGaussianBlur in="BackgroundImageFix" stdDeviation="2"/>\n' +
              '<feComposite in2="SourceAlpha" operator="in" result="effect1_backgroundBlur_16_214"/>\n' +
              '<feBlend mode="normal" in="SourceGraphic" in2="effect1_backgroundBlur_16_214" result="shape"/>\n' +
              '</filter>\n' +
              '<filter id="filter1_b_16_214" x="6.61371" y="9.26617" width="40.7748" height="38.186" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">\n' +
              '<feFlood flood-opacity="0" result="BackgroundImageFix"/>\n' +
              '<feGaussianBlur in="BackgroundImageFix" stdDeviation="2"/>\n' +
              '<feComposite in2="SourceAlpha" operator="in" result="effect1_backgroundBlur_16_214"/>\n' +
              '<feBlend mode="normal" in="SourceGraphic" in2="effect1_backgroundBlur_16_214" result="shape"/>\n' +
              '</filter>\n' +
              '</defs>\n' +
              '</svg>\n'
        },
        BNB: {
          name: 'BNB',
          icon: '<svg width="67" height="61" viewBox="0 0 67 61" fill="none" xmlns="http://www.w3.org/2000/svg">\n' +
              '<g filter="url(#filter0_d_16_250)">\n' +
              '<path fill-rule="evenodd" clip-rule="evenodd" d="M6 33L12 27L6 21L0 27L6 33Z" fill="#FFE600"/>\n' +
              '</g>\n' +
              '<g filter="url(#filter1_d_16_250)">\n' +
              '<path fill-rule="evenodd" clip-rule="evenodd" d="M48 33L54 27L48 21L42 27L48 33Z" fill="#FFE600"/>\n' +
              '</g>\n' +
              '<g filter="url(#filter2_d_16_250)">\n' +
              '<path fill-rule="evenodd" clip-rule="evenodd" d="M27 33L33 27L27 21L21 27L27 33Z" fill="#FFE600"/>\n' +
              '</g>\n' +
              '<g filter="url(#filter3_d_16_250)">\n' +
              '<path fill-rule="evenodd" clip-rule="evenodd" d="M30 3L27 1.68619e-08L10.5 16.5L16.5 22.5L27 12L37.5 22.5L43.5 16.5L30 3Z" fill="#FFE600"/>\n' +
              '</g>\n' +
              '<g filter="url(#filter4_d_16_250)">\n' +
              '<path fill-rule="evenodd" clip-rule="evenodd" d="M24 51L27 54L43.5 37.5L37.5 31.5L27 42L16.5 31.5L10.5 37.5L24 51Z" fill="#FFE600"/>\n' +
              '</g>\n' +
              '<defs>\n' +
              '<filter id="filter0_d_16_250" x="0" y="21" width="25" height="24" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">\n' +
              '<feFlood flood-opacity="0" result="BackgroundImageFix"/>\n' +
              '<feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha"/>\n' +
              '<feOffset dx="9" dy="8"/>\n' +
              '<feGaussianBlur stdDeviation="2"/>\n' +
              '<feComposite in2="hardAlpha" operator="out"/>\n' +
              '<feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.5 0"/>\n' +
              '<feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_16_250"/>\n' +
              '<feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_16_250" result="shape"/>\n' +
              '</filter>\n' +
              '<filter id="filter1_d_16_250" x="42" y="21" width="25" height="24" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">\n' +
              '<feFlood flood-opacity="0" result="BackgroundImageFix"/>\n' +
              '<feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha"/>\n' +
              '<feOffset dx="9" dy="8"/>\n' +
              '<feGaussianBlur stdDeviation="2"/>\n' +
              '<feComposite in2="hardAlpha" operator="out"/>\n' +
              '<feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.5 0"/>\n' +
              '<feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_16_250"/>\n' +
              '<feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_16_250" result="shape"/>\n' +
              '</filter>\n' +
              '<filter id="filter2_d_16_250" x="21" y="21" width="25" height="24" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">\n' +
              '<feFlood flood-opacity="0" result="BackgroundImageFix"/>\n' +
              '<feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha"/>\n' +
              '<feOffset dx="9" dy="8"/>\n' +
              '<feGaussianBlur stdDeviation="2"/>\n' +
              '<feComposite in2="hardAlpha" operator="out"/>\n' +
              '<feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.5 0"/>\n' +
              '<feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_16_250"/>\n' +
              '<feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_16_250" result="shape"/>\n' +
              '</filter>\n' +
              '<filter id="filter3_d_16_250" x="10.5" y="0" width="46" height="34.5" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">\n' +
              '<feFlood flood-opacity="0" result="BackgroundImageFix"/>\n' +
              '<feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha"/>\n' +
              '<feOffset dx="9" dy="8"/>\n' +
              '<feGaussianBlur stdDeviation="2"/>\n' +
              '<feComposite in2="hardAlpha" operator="out"/>\n' +
              '<feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.5 0"/>\n' +
              '<feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_16_250"/>\n' +
              '<feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_16_250" result="shape"/>\n' +
              '</filter>\n' +
              '<filter id="filter4_d_16_250" x="10.5" y="31.5" width="46" height="34.5" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">\n' +
              '<feFlood flood-opacity="0" result="BackgroundImageFix"/>\n' +
              '<feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha"/>\n' +
              '<feOffset dx="9" dy="8"/>\n' +
              '<feGaussianBlur stdDeviation="2"/>\n' +
              '<feComposite in2="hardAlpha" operator="out"/>\n' +
              '<feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.5 0"/>\n' +
              '<feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_16_250"/>\n' +
              '<feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_16_250" result="shape"/>\n' +
              '</filter>\n' +
              '</defs>\n' +
              '</svg>\n'
        },
        LC: {
          name: "Lite Coin",
          icon: '<svg width="76" height="61" viewBox="0 0 76 61" fill="none" xmlns="http://www.w3.org/2000/svg">\n' +
              '<g filter="url(#filter0_di_16_268)">\n' +
              '<path fill-rule="evenodd" clip-rule="evenodd" d="M26 52C40.3594 52 52 40.3594 52 26C52 11.6406 40.3594 0 26 0C11.6406 0 0 11.6406 0 26C0 40.3594 11.6406 52 26 52ZM18.1651 25.8391L14.8784 27.0566L13.9495 30.6704L17.2009 29.5192L15.0632 37.856H36.7338L38.064 32.9141H24.7154L26.3747 26.198L30.0329 24.8711L30.8926 21.206L27.453 22.4617L30.1592 11.856H21.8876L18.1651 25.8391Z" fill="#29ABE2"/>\n' +
              '</g>\n' +
              '<defs>\n' +
              '<filter id="filter0_di_16_268" x="0" y="0" width="76" height="136" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">\n' +
              '<feFlood flood-opacity="0" result="BackgroundImageFix"/>\n' +
              '<feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha"/>\n' +
              '<feOffset dx="20" dy="80"/>\n' +
              '<feGaussianBlur stdDeviation="2"/>\n' +
              '<feComposite in2="hardAlpha" operator="out"/>\n' +
              '<feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0"/>\n' +
              '<feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_16_268"/>\n' +
              '<feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_16_268" result="shape"/>\n' +
              '<feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha"/>\n' +
              '<feOffset dx="9" dy="9"/>\n' +
              '<feGaussianBlur stdDeviation="35"/>\n' +
              '<feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1"/>\n' +
              '<feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0"/>\n' +
              '<feBlend mode="normal" in2="shape" result="effect2_innerShadow_16_268"/>\n' +
              '</filter>\n' +
              '</defs>\n' +
              '</svg>\n'
        },
        ETH: {
          name: "Ethereum",
          icon: '<svg width="54" height="54" viewBox="0 0 54 54" fill="none" xmlns="http://www.w3.org/2000/svg">\n' +
              '<circle cx="27" cy="27" r="27" fill="black"/>\n' +
              '<path fill-rule="evenodd" clip-rule="evenodd" d="M13.1447 27L27.3552 4.26312V20.878L13.1447 27ZM40.8552 27L27.3552 20.8861V4.26312L40.8552 27Z" fill="#828384"/>\n' +
              '<path fill-rule="evenodd" clip-rule="evenodd" d="M27.3552 35.5261L13.1447 27.5334L27.3552 21.3156V35.5261ZM40.8552 27.5348L27.3552 35.5261V21.3156L40.8552 27.5348Z" fill="#343535"/>\n' +
              '<path fill-rule="evenodd" clip-rule="evenodd" d="M13.1447 30.5526L27.3552 38.7557V49.7368L13.1447 30.5526ZM40.8552 30.5526L27.3552 49.7368V38.7548L40.8552 30.5526Z" fill="#828384"/>\n' +
              '<path fill-rule="evenodd" clip-rule="evenodd" d="M40.8552 27L27.3552 20.8861V4.26312L40.8552 27Z" fill="white" fill-opacity="0.7"/>\n' +
              '<path fill-rule="evenodd" clip-rule="evenodd" d="M40.8552 27.5348L27.3552 21.3156V35.5261L40.8552 27.5348Z" fill="#131313"/>\n' +
              '<path fill-rule="evenodd" clip-rule="evenodd" d="M40.8552 30.5526L27.3552 38.7548V49.7368L40.8552 30.5526Z" fill="white" fill-opacity="0.7"/>\n' +
              '</svg>\n'
        }
      },
      transactions: {
        1: 'Buy',
        2: 'Recieved',
        3: 'Widthdrawal',
      }
    };
  },
}
</script>

<style lang="scss">
div.transaction{
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  padding: 10px 0;
  h3{
    font-size: 14px;
    font-weight: 500;
    margin: 0;
  }
  p.value{
    color: #4AD619;
  }
  &.negative{
    p.value{
      color: #FF0000;
    }
  }
}
</style>