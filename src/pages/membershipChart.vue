<template>
  <div class="line">
    <q-card bordered class="bg-white-9 my-card">
      <q-separator dark inset />

      <q-card-section class="chart-section">
        <div class="full">
          <b class="text">Monthly Membership Reports</b>
        </div>
        <canvas id="myChart8" width="530" height="200"></canvas
      ></q-card-section>
    </q-card>
  </div>
</template>
<script>
import Chart from "chart.js/auto";

export default {
  name: "memebershipChart",
  mounted: function () {
    const ctx = document.getElementById("myChart8");
    const myChart7 = new Chart(ctx, {
      type: "line",
      data: {
        labels: [
          "1-7 April",
          "8-14 April",
          "15-21 April",
          "22-28 April",
          "29-30 April",
        ],
        datasets: [
          {
            label: "# of Votes",
            data: [30000, 20000, 50000, 27000, 7000],
            backgroundColor: "	#FFC0CB",

            borderColor: "#FF69B4",

            tension: 0.4,
            borderWidth: 2,
            fill: true,
          },
        ],
      },
      options: {
        scales: {
          y: {
            beginAtZero: true,
            grid: { display: false, drawBorder: false },
          },
          x: { grid: { display: false, drawBorder: false } },
        },
        ticks: {
          min: 0,
          max: 30000,
          stepSize: 5000,
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
    myChart8;
  },
};
</script>
<style scoped>
.line {
  width: 500px;
  height: 250px;
}
.date {
  font-size: 0.8rem;
  color: silver;
  margin-left: 40%;
  /* margin-bottom:5%; */
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
  width: 13rem;
  height: 0.1rem;
  border: none;
  margin-left: -0.4%;
  margin-top: -2%;
  background-color: red;
}
.my-card {
  border-radius: 2%;
  width: 550px;
}
.text {
  margin-left: 155px;
  margin-bottom: 10%;
}
.full {
  display: flex;
  flex-direction: column;
}
</style>





<!-- //<h3 class="first">Total Events Registrations<hr class="hrline"/></h3> -->
