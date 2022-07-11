<template>
  <div class="bg">
    <h6 class="h6">Dashboard</h6>
    <hr class="hr" />

    <b> <label id="monthText">Select Month Range</label></b>
    <b> <label id="monthText2">Select Month Range</label></b>
    <div class="dateTop">
      <DateChart class="date1" />
      <DateChart1 class="date2" />
    </div>
    <div class="visitGraph">
      <VisitorChart class="visit" />
      <MembershipChart class="member" />
    </div>
    <div class="table2">
      <CourseName1 class="course1" />
      <CourseName2 class="course1" />
    </div>
    <div class="graphs">
      <LineChart class="line" />
      <CybertalkChart class="cyber" />
      <TotalChart />
    </div>

    <div class="graphs2">
      <CourseName class="course" />
      <AspenChart class="aspen" />
    </div>
    <div class="table3">
      <AccountLinked class="account" />
      <PlatForm class="platForm" />
    </div>
    <BrowserChart class="browser" />
  </div>
</template>

<script>
import { defineComponent, ref } from "vue";
import DateChart from "src/pages/dateChart.vue";
import DateChart1 from "src/pages/dateChart.vue";
import VisitorChart from "src/pages/visitorChart.vue";
import MembershipChart from "src/pages/membershipChart.vue";
import CourseName1 from "src/pages/courseName1.vue";
import CourseName2 from "src/pages/courseName2.vue";
import LineChart from "src/pages/lineChart.vue";
import CybertalkChart from "src/pages/cybertalkChart.vue";
import TotalChart from "src/pages/totalChart.vue";
import CourseName from "src/pages/courseName.vue";
import AspenChart from "src/pages/aspenChart.vue";
import AccountLinked from "src/pages/accountLinked.vue";
import PlatForm from "src/pages/platForm.vue";
import BrowserChart from "src/pages/browserChart.vue";

export default defineComponent({
  name: "MainLayout",

  components: {
    DateChart,
    DateChart1,
    VisitorChart,
    MembershipChart,
    CourseName1,
    CourseName2,
    LineChart,
    CybertalkChart,
    TotalChart,
    CourseName,
    AspenChart,
    AccountLinked,
    PlatForm,
    BrowserChart,
  },
});
</script>
<style scoped>
.h6 {
  text-align: center;
  font-weight: 600;
}
.graphs {
  display: flex;
  flex-direction: row;
  margin-left: 1%;
  margin-top: 5%;
  gap: 1.8rem;
}
.line {
  text-align: left;
  justify-content: center;
}
.graphs2 {
  display: flex;
  flex-direction: row;
  margin-top: 5.5%;
  margin-left: 1%;
  gap: 12.8rem;
}

.visitGraph {
  display: flex;
  flex-direction: row;
  margin-top: 5%;
  margin-left: 1.5%;
  gap: 9.5rem;
}
.hr {
  width: 5%;
  margin-top: -3%;
  background-color: red;
  height: 0.1rem;
  border: none;
  margin-bottom: 4%;
}
.visit {
  /* margin-left: -70%; */
}
.date {
  margin-left: 15%;
  margin-bottom: -5%;
}
.browser {
  gap: 2rem;
  margin-top: -2%;
  margin-left: 0.8%;
}
.bg {
  background-color: #f0f0f08b;
  height: 100% auto;
}
.table2 {
  display: flex;
  flex-direction: row;
  gap: 14rem;
  margin-left: none;
  margin-bottom: -4%;
  margin-top: 4%;
}

.dateTop {
  /* margin-left: 15%;
  margin-bottom:-5%; */
  display: flex;
  flex-direction: row;
  gap: 29em;
  margin-left: 1.5%;
  /* height: 90px; */
  margin-bottom: -6%;
}
#monthText {
  margin-left: 8.5%;

  /* margin-top: -12px; */
}
#monthText2 {
  margin-left: 38%;
  /* margin-top: -12px; */
}
.date1 {
  /* background-color: white; */
}
.table3 {
  display: flex;
  flex-direction: row;
  margin-bottom: 20%;
  gap: 9.8rem;
  margin-left: 2%;
}
</style>
