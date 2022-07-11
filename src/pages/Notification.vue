<template>
  <div class="main_div">
    <div class="details">
      <div class="certificates">
        <p class="label">My Certificates</p>
        <p class="data">8</p>
      </div>
      <div class="certificates">
        <p class="label">My Registered Courses</p>
        <p class="data">8</p>
      </div>
      <div class="certificates">
        <p class="label">My Registered Events</p>
        <p class="data">8</p>
      </div>
    </div>
    <div class="announcements_button">
      <div class="buttons">
        <div>
          <img class="img" src="~src/assets/activity.svg" />
        </div>
        <div><p class="announcement_button">Membership Announcements</p></div>
        <div><q-link class="viewall">view All</q-link></div>
      </div>
      <q-card class="my-card">
        <q-card-section>
          <div class="notification_div">
            <div class="first_column">
              <img class="img1" src="~src/assets/bell.svg" />
              <div>
                jangra
                <p>fhfskdjfksddhfksdhfksdjf</p>
              </div>
            </div>
            <div>
              <p>5hr ago</p>
            </div>
          </div>
          <div class="announcement_div">
            <div class="first_column">
              <img class="img2" src="~src/assets/target.svg" />
              <div>
                jangra this si ak
                <p>fhfskdjfksddhfksdhfksdjf</p>
              </div>
            </div>

            <div>
              <p>5hr ago</p>
            </div>
          </div>
          <div class="notification_div">
            <div class="first_column">
              <img class="img1" src="~src/assets/bell.svg" />
              <div>
                jangra
                <p>fhfskdjfksddhfksdhfksdjf</p>
              </div>
            </div>
            <div>
              <p>5hr ago</p>
            </div>
          </div>
          <div class="announcement_div">
            <div class="first_column">
              <img class="img2" src="~src/assets/target.svg" />
              <div>
                jangra this si ak
                <p>fhfskdjfksddhfksdhfksdjf</p>
              </div>
            </div>

            <div>
              <p>5hr ago</p>
            </div>
          </div>
        </q-card-section>
      </q-card>
    </div>
  </div>
</template>

<script>
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "NotiFication",
  setup() {
    return {};
  },
});
</script>

<style scoped>
.main_div {
  display: flex;
  height: 25%;
  /* background-color: rgb(198,  198, 198); */
}
.details {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  text-align: center;
  width: 15%;
  /* padding: 1%; */
  /* margin-bottom: -5px; */
  font-weight: 700;
  padding-top: 20px;
}
.buttons {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.announcement_button {
  font-size: 12px;
  font-weight: 600;
}
.viewall {
  font-size: 10px;
}
.label {
  font-size: 12px;
  margin: 0px;
}
.data {
  font-size: 18px;
  margin: 0px;
}
.certificates {
  /* line-height: 17px; */
  box-shadow: 0px 0px 10px 2px rgba(1, 1, 1, 0.3);
  height: 60px;
  border-radius: 10px;
  margin: 0px 20px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.my-card {
  font-size: 10px;
  box-shadow: 0px 0px 10px 2px rgba(1, 1, 1, 0.3);
  /* margin-bottom:10px; */
}
.announcements_button {
  width: 100%;
  max-width: 250px;
}
p {
  font-size: 8px;
}
.first_column {
  display: flex;
}
.img1 {
  height: 27px;
  margin-right: 9px;
}
.img2 {
  height: 27px;
  margin-right: 9px;
}
.notification_div {
  display: flex;
  justify-content: space-between;
}
.announcement_div {
  display: flex;
  justify-content: space-between;
}
</style>
