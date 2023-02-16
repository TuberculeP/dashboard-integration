<template>
  <div class="chart">
    <div class="chart-header">
      <nav class="time-select">
        <ul>
          <li>1H</li>
          <li class="active">1D</li>
          <li>3D</li>
          <li>1W</li>
          <li>1M</li>
          <li><svg width="26" height="26" viewBox="0 0 26 26" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M23.1111 2.6H21.6667V0H18.7778V2.6H7.22222V0H4.33333V2.6H2.88889C1.28556 2.6 0.0144444 3.77 0.0144444 5.2L0 23.4C0 24.83 1.28556 26 2.88889 26H23.1111C24.7 26 26 24.83 26 23.4V5.2C26 3.77 24.7 2.6 23.1111 2.6ZM23.1111 23.4H2.88889V9.1H23.1111V23.4ZM5.77778 11.7H13V18.2H5.77778V11.7Z"/>
          </svg>
          </li>
        </ul>
      </nav>
      <div class="compare">
        <div class="currency">
          <svg width="31" height="31" viewBox="0 0 31 31" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path fill-rule="evenodd" clip-rule="evenodd" d="M14.4804 16.3527L17.3384 16.2722C18.6722 16.2346 19.4909 17.1026 19.4948 18.3753C19.5206 19.2974 19.1308 20.1358 18.3776 20.4752C18.0954 20.6104 17.6834 20.6538 17.3341 20.6636L14.6032 20.7406L14.4804 16.3527ZM17.8752 10.4656C18.4556 10.7675 18.7592 11.3953 18.7797 12.1266C18.8117 13.2713 18.1671 14.085 17.0239 14.1172L14.4199 14.1906L14.3123 10.3432L16.5988 10.2788C17.1068 10.2645 17.5532 10.3156 17.8752 10.4656ZM17.6496 22.8504C17.6911 24.3343 17.7118 25.0763 17.7118 25.0763C17.7118 25.0763 17.2143 25.0903 16.2193 25.1183L16.157 22.8925L14.601 22.9363C14.6425 24.4202 14.6633 25.1622 14.6633 25.1622C14.6633 25.1622 14.1658 25.1762 13.1708 25.2042L13.1085 22.9784C11.1185 23.0345 10.1235 23.0625 10.1235 23.0625C10.1235 23.0625 10.1045 22.3842 10.0666 21.0276L10.9875 21.0017C11.4638 20.9883 11.8025 20.5968 11.79 20.1517L11.5383 11.1533C11.525 10.6764 11.1342 10.3374 10.6896 10.3499C10.0757 10.3672 9.76869 10.3759 9.76869 10.3759C9.76869 10.3759 9.74972 9.69752 9.71177 8.34084L12.6968 8.25673C12.6553 6.7729 12.6346 6.03099 12.6346 6.03099C12.6346 6.03099 13.1321 6.01697 14.127 5.98894L14.1893 8.21468L15.7453 8.17084C15.7038 6.68701 15.683 5.9451 15.683 5.9451C15.683 5.9451 16.1805 5.93108 17.1756 5.90304L17.2387 8.16054C18.0017 8.17089 18.6077 8.2493 19.2182 8.48668C20.5661 8.9578 21.5218 10.1719 21.568 11.8253C21.6071 13.2244 21.004 14.387 19.8459 15.0242C21.5123 15.5182 22.2827 16.9284 22.3263 18.4865C22.3506 20.4905 21.0577 21.9907 19.4842 22.5442C18.8545 22.7529 18.2847 22.8325 17.6496 22.8504ZM0.422407 15.9533C0.655398 24.2839 7.60862 30.8661 15.9286 30.6316C24.2484 30.3972 30.8229 23.4339 30.5899 15.1033C30.3569 6.77265 23.4036 0.190586 15.0837 0.425006C6.76381 0.659429 0.189417 7.62265 0.422407 15.9533Z" fill="white"/>
          </svg>
          <p>BTC</p>
          <svg width="20" height="13" viewBox="0 0 20 13" fill="none" xmlns="http://www.w3.org/2000/svg" class="arrow">
            <path opacity="0.7" d="M16.9535 0.56604L9.75319 7.90141L2.55284 0.56604L0.340973 2.82431L9.75319 12.434L19.1654 2.82431L16.9535 0.56604Z" fill="white"/>
          </svg>
        </div>
        <svg width="37" height="25" viewBox="0 0 37 25" fill="none" xmlns="http://www.w3.org/2000/svg" class="compare">
          <g opacity="0.7">
            <path d="M29.2111 14.0777L36.25 7.03883L29.2111 0V5.27912H2.81552V8.79854H29.2111V14.0777Z" fill="white"/>
            <path d="M7.03883 10.3236L0 17.3624L7.03883 24.4013V19.1221H33.4345V15.6027H7.03883V10.3236Z" fill="white"/>
          </g>
        </svg>
        <div class="currency">
          <svg width="31" height="31" viewBox="0 0 31 31" fill="none" xmlns="http://www.w3.org/2000/svg">
            <ellipse cx="15.09" cy="15.11" rx="15.09" ry="15.11" fill="white"/>
            <path fill-rule="evenodd" clip-rule="evenodd" d="M7.34644 15.11L15.2885 2.3858V11.684L7.34644 15.11ZM22.8335 15.11L15.2885 11.6885V2.3858L22.8335 15.11Z" fill="#828384"/>
            <path fill-rule="evenodd" clip-rule="evenodd" d="M15.2885 19.8816L7.34644 15.4086L15.2885 11.929V19.8816ZM22.8335 15.4094L15.2885 19.8816V11.929L22.8335 15.4094Z" fill="#343535"/>
            <path fill-rule="evenodd" clip-rule="evenodd" d="M7.34644 17.0981L15.2885 21.6889V27.8342L7.34644 17.0981ZM22.8335 17.0981L15.2885 27.8342V21.6883L22.8335 17.0981Z" fill="#828384"/>
            <path fill-rule="evenodd" clip-rule="evenodd" d="M22.8335 15.11L15.2885 11.6885V2.3858L22.8335 15.11Z" fill="#2F3030"/>
            <path fill-rule="evenodd" clip-rule="evenodd" d="M22.8335 15.4094L15.2885 11.929V19.8816L22.8335 15.4094Z" fill="#131313"/>
            <path fill-rule="evenodd" clip-rule="evenodd" d="M22.8335 17.0981L15.2885 21.6883V27.8342L22.8335 17.0981Z" fill="#2F3030"/>
          </svg>
          <p>ETH</p>
          <svg width="20" height="13" viewBox="0 0 20 13" fill="none" xmlns="http://www.w3.org/2000/svg" class="arrow">
            <path opacity="0.7" d="M16.9535 0.56604L9.75319 7.90141L2.55284 0.56604L0.340973 2.82431L9.75319 12.434L19.1654 2.82431L16.9535 0.56604Z" fill="white"/>
          </svg>
        </div>
      </div>
    </div>
    <div class="main-chart">
      <canvas id="mainChart"></canvas>
    </div>
  </div>
</template>

<script>
import Chart from 'chart.js'

export default {
  name: "MainChart",
  mounted() {
    new Chart(document.getElementById("mainChart").getContext('2d'), {
      type: "line",
      data: {
        labels: [
          '5Nov',
          '6Nov',
          '7Nov',
          '8Nov',
          '9Nov',
          '10Nov',
          '11Nov',
          '12Nov',
          '13Nov',
          '14Nov',
          '15Nov',
        ],
        datasets: [
          {
            label: 'ETH',
            data: [100, 400, 600, 400, 300, 100, 300, 200, 300, 400, 100],
            borderColor: '#716b94',
            backgroundColor: 'transparent',
          },
          {
            label: 'BTC',
            data: [100, 600, 200, 200, 100, 400, 100, 400, 600, 500, 1000],
            borderColor: '#FAFF00',
            backgroundColor: 'transparent',
          },
        ],
      },
      options: {
        responsive: true,
        maintainAspectRatio: false,
        legend: {
          display: false,
        },
        scales: {
          yAxes: [{
            ticks: {
              fontColor: 'rgba(255,255,255,0.8)',
              fontSize: 14,
              callback: (value)=>{return '$' + value}
            },
            gridLines: {
              display: false,
            },
          }],
          xAxes: [{
            ticks: {
              fontColor: 'rgba(255,255,255,0.8)',
              fontSize: 14,
            },
            gridLines: {
              display: false,
            }
          }]
        }
      }
    })
    document.querySelectorAll('.time-select li').forEach((item)=>{
      item.addEventListener('click', (e)=>{
        let active = document.querySelector('.time-select li.active')
        if(active) active.classList.remove('active')
        e.target.classList.add('active')
      })
    })
  }
}
</script>

<style scoped lang="scss">
div.chart{
  width: 100%;
  margin: 0 auto;
  background-color: #303541AB;
  border-radius: 1rem;
  padding: 30px;
  .chart-header{
    display: flex;
    justify-content: space-between;
    align-items: center;
    nav.time-select{
      ul{
        display: flex;
        align-items: center;
        gap: 5px;
        li{
          list-style: none;
          cursor: pointer;
          height: fit-content;
          background-color: black;
          padding: 5px;
          border-radius: 0.3rem;
          width: 1.6rem;
          aspect-ratio: 1/1;
          line-height: 1rem;
          font-size: 0.8rem;
          text-align: center;
          &.active, &:hover{
            background-color: #ffffff;
            color: #000000;
            opacity: 0.8;
            cursor: pointer;
            svg{
              fill: black;
            }
          }
          svg{
            width: 0.8rem;
            height: 0.8rem;
            fill: #fff;
            display: block;
            margin: 0 auto;
          }
        }
      }
    }
    div.compare{
      display: flex;
      align-items: center;
      gap: 0.5rem;
      svg.compare{
        height: 1rem;
      }
      div.currency{
        display: flex;
        align-items: center;
        gap: 5px;
        background-color: black;
        padding: 0.2rem 0.8rem;
        &:hover{
          cursor: pointer;
        }
        p{
          font-size: 0.8rem;
          color: #fff;
          user-select: none;
        }
        svg{
          width: 0.8rem;
          height: 0.8rem;
          &.arrow {
            margin-left: 1rem;
          }
        }
      }
    }
  }
  div.main-chart{
    position: relative;
    padding-top: 30px;
    width: 100%;
    height: 100%;
  }
}
</style>