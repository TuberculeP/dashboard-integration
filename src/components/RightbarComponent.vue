<template>
  <div class="rightbar">
    <div class="close">
      <div>
        <div class="line"></div>
        <div class="line"></div>
      </div>
    </div>
    <RightbarNav/>
    <div>
      <h2>Recent Transactions</h2>
      <div class="transactions">
        <RightbarTransactions currency="USDT" transaction_type=2 transaction_value=3546 date="Today, 13:45 pm"/>
        <RightbarTransactions date="Today, 5:45 am" transaction_value=0.7546 transaction_type=2 currency="BNB"/>
        <RightbarTransactions date="Today 7:55 am" transaction_value=-0.7546 transaction_type=3 currency="LC"/>
        <RightbarTransactions date="Today 8:55 am" transaction_value=2.7546 transaction_type=2 currency="BTC"/>
        <RightbarTransactions date="Today 10:02 am" transaction_value=1.646 transaction_type=2 currency="ETH"/>
      </div>
    </div>
    <div>
      <h2>Assets</h2>
      <div class="assets">
        <RightbarAsset currency="BTC" asset_value="1216450.45"/>
        <RightbarAsset currency="ETH" asset_value="143850.45"/>
      </div>
    </div>
  </div>
</template>

<script>
import RightbarNav from "@/components/Rightbar/RightbarNav.vue";
import RightbarTransactions from "@/components/Rightbar/RightbarTransactions.vue";
import RightbarAsset from "@/components/Rightbar/RightbarAsset.vue";

export default {
  name: "RightbarComponent",
  components: {RightbarAsset, RightbarTransactions, RightbarNav}
}
</script>

<style scoped lang="scss">
div.rightbar{
  position: relative;
  padding: 30px;
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: repeat(3, 1fr);
  h2{
    padding: 50px 20px 0;
  }
  div.transactions{
    overflow: scroll;
    ::-webkit-scrollbar {
      width: 0;
      background: transparent;
    }
  }
}
div.close{
  display: none;

}
@media screen and (max-width: 768px){
  div.close{
    display: flex;
    justify-content: flex-end;
    div{
      position: relative;
      cursor: pointer;
      width: 30px;
      height: 30px;
      .line{
        position: absolute;
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