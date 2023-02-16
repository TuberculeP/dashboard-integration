<template>
  <div>
    <MainHeader/>
    <main>
      <MainBalance/>
      <MainChart/>
      <div>
        <div class="transactions">
          <h4 class="active">Recent Transactions</h4>
          <h4>See all coins</h4>
        </div>
        <MainTransaction currency="BTC" MarketCap="40243.70" DayChange="1.56"/>
        <MainTransaction currency="ETH" MarketCap="40243.70" DayChange="-1.56"/>
      </div>
    </main>
  </div>
</template>

<script>
import MainHeader from '@/components/Main/MainHeader.vue'
import MainBalance from "@/components/Main/MainBalance.vue";
import MainChart from "@/components/Main/MainChart.vue";
import MainTransaction from "@/components/Main/MainTransaction.vue";
export default {
  name: "MainComponent",
  components: {
    MainTransaction,
    MainHeader,
    MainBalance,
    MainChart,
  },
  mounted() {
    document.querySelectorAll("h4").forEach((h4) => {
      h4.addEventListener("click", () => {
        document.querySelector("h4.active").classList.remove("active");
        h4.classList.add("active");
      });
    });
  }
}
</script>

<style scoped lang="scss">
main{
  display: grid;
  grid-template-rows: 1fr 300px 1.5fr;
}

.transactions{
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 1rem;
  h4{
    margin: 0 25px;
    font-size: 1.2rem;
    font-weight: 500;
    color: #9B9B9B;
    cursor: pointer;
    &.active{
      color: white;
    }
  }
}
</style>