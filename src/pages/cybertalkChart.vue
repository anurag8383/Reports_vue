<template>
  <div class="line">
    <h3 class="first">
      CyberTalks Registrations
      <hr class="hrline" />
    </h3>
    <q-card bordered class="bg-white-9 my-card">
      <q-separator dark inset />

      <q-card-section class="chart-section">
        <label class="date">15 April - 12 May</label>
        <canvas id="myChart2" width="350" height="200"></canvas
      ></q-card-section>
    </q-card>
  </div>
</template>
<script>
import Chart from "chart.js/auto";

export default {
  name: "cybertalkChart",
  mounted: function () {
    const ctx = document.getElementById("myChart2");
    const myChart1 = new Chart(ctx, {
      type: "line",
      data: {
        labels: [
          "15 April",
          "21 April",
          "22 April",
          "29 April",
          "5 May",
          "12 May",
        ],
        datasets: [
          {
            label: "# of Votes",
            data: [258, 250, 300, 400, 350, 375],
            backgroundColor: "rgba(255, 99, 132, 0.2)",

            borderColor: "rgb(100,149,237)",

            tension: 0.4,
            borderWidth: 2,
          },
        ],
      },
      options: {
        scales: {
          y: {
            beginAtZero: true,
            grid: { display: false, drawBorder: false },
          },
          x: {
            grid: {
              offset: true,
              color: "rgb(135,206,235)",

              tickColor: "white",

              //  display: false, drawBorder: false
            },
          },
        },
        ticks: {
          min: 0,
          max: 500,
          stepSize: 250,
          fontColor: "#000",
          fontSize: 14,
        },
        elements: {
          point: {
            radius: 0,
          },
        },

        plugins: {
          legend: {
            display: false,
            labels: {
              color: "rgb(255, 99, 132)",
            },
          },
        },
        responsive: false,
        chartArea: {
          backgroundColor: "rgba(251, 85, 85, 0.4)",
        },
      },
    });
    myChart2;
  },
};
</script>
<style scoped>
.line {
  width: 400px;
  height: 250px;
}
.date {
  font-size: 0.8rem;
  color: silver;
  margin-left: 40%;
  margin-bottom: 5%;
  /* justify-content: center;
  text-align: center; */
}
.first {
  font-size: 1.5rem;
}
.hrline {
  width: 20rem;
}
.first {
  font-size: 1.2rem;
  font-weight: 600;
}
.hrline {
  width: 14rem;
  height: 0.1rem;
  border: none;
  margin-left: -0.5%;
  margin-top: -2%;
  background-color: red;
}
.my-card {
  border-radius: 3%;
}
</style>
