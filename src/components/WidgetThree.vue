<template>
  <div class="widgetThree">
    <h1 id="WidgetTittleThree">Balance</h1>
    <div class="graphWThree">
      <canvas ref="chart" id="chart"></canvas>
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
      const WtThree = this.$refs.chart.getContext('2d')
      new Chart(WtThree, {
        type: 'line',
        data: {
          labels: ['April', 'May', 'June'],
          datasets: [
            {
              label: ['April', 'May', 'June'],
              data: [4500, 15000, 500],
              fill: true,
              backgroundColor: [
                'rgb(64, 115, 158)',
                'rgb(229, 80, 57,0.9)',
                'rgb(164, 176, 190,0.9)',
                'rgb(255, 165, 2,0.7)'
              ],
              borderColor: 'rgb(47, 54, 64)',
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
body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  position: relative;
}
.widgetThree {
  background: #f3a683;
  height: 28rem;
  width: 39rem;
  position: absolute;
  left: 260px;
  top: 45.8rem;
  border-radius: 20px; /* Rounded corners */
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Soft shadow */
  transition: all 0.5s ease;
  /* border-radius: 20px; */
}
.One {
  color: red;
}

#WidgetTittleThree {
  position: relative;
  left: 240px;
}

/* canvas{
    color: rgb(64, 115, 158);
} */

.graphWThree {
  position: relative;
  left: 60px;
  bottom: -25px;
  height: 70rem;
  width: 500px;
  display: flex;
}
</style>
