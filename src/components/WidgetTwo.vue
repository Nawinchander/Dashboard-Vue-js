<template>
    <div class="widgetTwo">
        <h1 id="WidgetTittleTwo">Amount Spent</h1>
    <div class="graphWTwo">
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
      const WtTwo = this.$refs.chart.getContext('2d')
      new Chart(WtTwo, {
        type: 'bar',
        data: {
          labels: ['April', 'May', 'June'],
          datasets: [
            {
            //   label: ['April', 'May', 'June'],
              data: [37000, 50000, 25000],
              fill: false,
              backgroundColor: [
                'rgb(235, 77, 75)',
                'rgb(48, 51, 107)',
                'rgb(235, 47, 6)'
              ],
              borderColor: 'rgb(19, 15, 64)'
            //   tension: 1
            }
          ]
        },
        options: {
          scales: {
            y: {
              beginAtZero: true
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
.widgetTwo{
    background:#f6e58d;
    position: absolute;
    top: 274px;
    left:890px;
    right: 50px;
    height: 28rem;
    width: 39rem;
    border-radius: 20px; /* Rounded corners */
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Soft shadow */
    transition: all 0.5s ease;
}
.One{
    color: red;
}

#WidgetTittleTwo{
    position: relative;
    left: 217px;
}

.graphWTwo {
    position: relative;
    left: 70px;
    top: 25px;
  height: 500px;
  width: 500px;

}

</style>
