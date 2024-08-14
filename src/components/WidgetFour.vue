<template>
    <div class="widgetFour">

    <div class="Four">
        <h1 id="WidgetTittleFour">Expenses</h1>
    <div class="graphWFour">
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
      const WtFour = this.$refs.chart.getContext('2d')
      new Chart(WtFour, {
        type: 'doughnut',
        data: {
          labels: ['Entertainment', 'Travel', 'Partying', 'House', 'Insurance'],
          datasets: [
            {
              label: ['Entertainment', 'Travel', 'Partying', 'House', 'Insurance'],
              data: [5000, 10000, 20000, 50000, 30000],
              fill: true,
              backgroundColor: [
                'rgb(229, 80, 57,0.9)',
                'rgb(164, 176, 190,0.9)',
                'rgb(255, 165, 2,0.7)',
                'rgb(88, 177, 159)',
                'rgb(24, 44, 97,0.7)'
              ],
              borderColor: 'rgb(47, 53, 66)',
              tension: 2
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
.widgetFour{
    background:#ff9ff3;
    position: absolute;
    top: 45.8rem;
    left:890px;
    right: 190px;
    height: 28rem;
    width: 39rem;
    border-radius: 20px; /* Rounded corners */
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Soft shadow */
    transition: all 0.5s ease;
}
.One{
    color: red;
}

#WidgetTittleFour{
    position: relative;
    left: 248px;
}

.graphWFour{
    position: relative;
    left: 130px;
    bottom: 20px;
  height: 800px;
  width: 350px;
  display: flex;
}

</style>
