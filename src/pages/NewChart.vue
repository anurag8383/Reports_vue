<template>
  <div class="newChart">
    <canvas id="myChart" width="0.01" height="0.1"></canvas>
  </div>
</template>
<script>
import Chart from "chart.js/auto";

export default {
  name: "NewChart",
  mounted: function () {
    const ctx = document.getElementById("myChart");
    const myChart = new Chart(ctx, {
      type: "line",
      data: {
        labels: ["Jan", "Feb", "Mar", "Apr", "May", "Jun"],
        datasets: [
          {
            label: "# of Votes",
            data: [300, 350, 489, 370, 140, 200],
            backgroundColor: "rgba(255, 99, 132, 0.2)",

            borderColor: "rgba(255, 99, 132, 1)",

            tension: 0.4,
          },
        ],
      },
      options: {
        scales: {
          y: {
            beginAtZero: true,
          },
        },
      },
    });
    myChart;
  },
};
</script>
<style scoped>
.newChart {
  height: 300px;
  width: 500px;
}
</style>
