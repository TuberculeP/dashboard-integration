<template>
<div class="balance">
  <div class="flex">
    <div class="credits">
      <h3>Total Balance</h3>
      <p class="total">0.97894652</p>
    </div>
    <nav>
      <ul>
        <li class="active">Portfolio</li>
        <li>Funding</li>
        <li>Assets</li>
        <li>P2P</li>
      </ul>
    </nav>
  </div>
  <p class="converted">40,123.56</p>
</div>
</template>

<script>
export default {
  name: "MainBalance",
  mounted() {
    document.querySelectorAll('.balance nav ul li').forEach((item)=>{
      item.addEventListener('click', (e)=>{
        document.querySelector('.balance nav ul li.active').classList.remove('active')
        e.target.classList.add('active')
      })
    })
  }
}
</script>

<style scoped lang="scss">

div.balance{
  padding: 30px;
  div.flex{
    display: flex;
    align-items: center;
    gap: 20%;
    div.credits{
      h3{
        opacity: 0.8;
        font-size: 1rem;
        margin-bottom: 0.5rem;
      }
      p.total{
        position: relative;
        font-size: 1.5rem;
        font-weight: 600;
        &::after{
          content: "BTC";
          font-size: 0.6rem;
          position: absolute;
          top: 50%;
          right: -2rem;
          transform: translateY(-60%);
          background-color: #FAFF00;
          color: black;
          font-weight: bold;
          padding: 0.1rem 0.2rem;
          border-radius: 0.2rem;
        }
      }
    }
    nav{
      ul{
        list-style: none;
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 5px;
        background-color: #292727;
        padding: 10px 20px;
        border-radius: 0.8rem;
        li{
          padding: 0.1rem 0.5rem;
          border-radius: 0.5rem;
          cursor: pointer;
          &:hover{
            background-color: #0D0C0C;
            color: white;
          }
          &.active{
            background-color: #0D0C0C;
            color: white;

          }
        }
      }
    }
  }
  p.converted{
    margin-top: 0.5rem;
    font-weight: 500;
    opacity: 0.8;
    &::before{
      content: "$";
    }
  }
}

@media screen and (max-width: 768px){
  div.balance{
    div.flex{
      flex-direction: column;
      align-items: flex-start;
      gap: 0;
      width: 100%;
    }
  }
}

</style>