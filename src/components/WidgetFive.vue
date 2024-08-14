<template>
    <div class="widgetFive">

    <div class="Five">
        <h1 id="WidgetTittleFive">Total</h1>
    <div class="graphWFive">
    <canvas ref="chart" id="chart"></canvas>
     </div>

    </div>
    </div>
</template>

<script>
import Chart from 'chart.js/auto'
export default {
  mounted () {
    this.renderChart()
  },
  methods: {
    renderChart () {
      const WtFive = this.$refs.chart.getContext('2d')
      new Chart(WtFive, {
        type: 'polarArea',
        data: {
          labels: ['Wallet Recharge', 'Amount Spent', 'Balance', 'Expenses'],
          datasets: [
            {
              label: ['Wallet Recharge', 'Amount Spent', 'Balance', 'Expenses'],
              data: [5000, 10000, 20000, 50000],
              fill: true,
              backgroundColor: [
                'rgb(229, 80, 57,0.9)',
                'rgb(164, 176, 190,0.9)',
                'rgb(255, 165, 2,0.7)',
                'rgb(88, 177, 159)'
              ],
              borderColor: 'rgb(47, 53, 66)'
            //   tension: 2
            }
          ]
        },
        options: {
          scales: {
            y: {
              beginAtZero: false
            }
          }
        }
      })
    }
  }
}
</script>

<style>
body{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    position: relative;
}
.widgetFive{
    background:rgb(220, 221, 225);
    position: absolute;
    top: 74.8rem;
    left:265px;
    right: 190px;
    height: 28rem;
    width: 78rem;
    border-radius: 20px; /* Rounded corners */
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Soft shadow */
    transition: all 0.5s ease;
}
.One{
    color: red;
}

#WidgetTittleFive{
    position: relative;
    display: flex;
    justify-content: center;
}

.graphWFive{
    position: relative;
    left: 130px;
    bottom: 20px;
  height: 350px;
  width: 650px;
  display: flex;
}

</style>
