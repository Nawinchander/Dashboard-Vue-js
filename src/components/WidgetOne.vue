<!-- eslint-disable no-new -->
<!-- eslint-disable no-new -->
<!-- eslint-disable no-new -->
<!-- eslint-disable no-new -->
<template>
  <div class="widgetOne">
    <h1 id="WidgetTittleOne">Wallet Recharged</h1>
    <div class="graphWOne">
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
      const WtOne = this.$refs.chart.getContext('2d')
      new Chart(WtOne, {
        type: 'pie',
        data: {
          labels: ['April', 'May', 'June'],
          datasets: [
            {
              label: 'My First Dataset',
              data: [45, 15, 90],
              fill: false,
              backgroundColor: [
                'rgb(229, 80, 57,0.9)',
                'rgb(164, 176, 190,0.9)',
                'rgb(255, 165, 2,0.9)'
              ],
              borderColor: 'rgb(47, 53, 66)',
              tension: 1
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
template {
  padding: 50px;
}
body {
  margin: 0;
  padding: 30px;
  box-sizing: border-box;
  position: relative;
}

.widgetOne {
  border-radius: 20px;
  background: #b8e994;
  height: 28rem;
  width: 39rem;
  position: absolute;
  left: 261px;
  top: 274px;
  transition: all 0.3s ease;
  border-radius: 20px; /* Rounded corners */
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Soft shadow */
  transition: all 0.5s ease;
  /* border-radius: 20px; */
}

#WidgetTittleOne {
  position: relative;
  left: 165px;
}
.One {
  color: red;
}
.graphWOne {
    position: relative;
    left: 120px;
    top: -13px;
  height: 350px;
  width: 350px;
  display: flex;
}
</style>
