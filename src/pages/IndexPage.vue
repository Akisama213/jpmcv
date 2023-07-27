<template>
  <StaryBg :extend="extend" />
  <q-page class="CenturyGothic" style="overflow-x: hidden; left: 0.5%">
    <!--This section is used to animate my name-->
    <span @mouseover="extend = true" @mouseleave="extend = false">
      <h1 class="text-accent">
        Jason<NameAnim label="Piedra" :extend="extend" />
        <NameAnim label="Matamoros" :extend="extend" />
      </h1>
    </span>
    <h6>Frontend Developer | Software Developer</h6>

    <q-card class="card" dark flat key="crad0">
      <q-card-section horizontal>
        <q-img
          class="img_main_page"
          spinner-color="primary"
          src="images/sign.gif"
        />
        <q-card-section>
          <h3>Summary</h3>
          <q-list
            ><q-item-section
              ><q-item
                >Dependable Frontend Developer with creative and effective
                problem solving.</q-item
              ><q-item
                >Native Spanish speaker with excellent proficiency in English
                (C1).</q-item
              ><q-item
                >Invested in hard work and collaboration to get accurate
                solutions efficiently.</q-item
              ><q-item
                >Always willing to learn, be it from coworkers or
                self-studying.</q-item
              ><q-item
                >Detail-oriented professional focused in creating intuitive and
                innovative UIs.</q-item
              >
            </q-item-section>
          </q-list>
        </q-card-section>
      </q-card-section>
    </q-card>
    <q-card class="card" dark flat>
      <q-card-section horizontal>
        <q-card-section>
          <h3>Education</h3>
          <q-list
            ><q-item-section
              ><q-item>
                Liceo Experimental Bilingüe 2014 - 2019 High School Diploma -
                Conversational English Diploma</q-item
              ><q-item>
                Tecnológico de Costa Rica 2020 - 2024 Bachelor’s Degree in
                Computer Engineering
              </q-item></q-item-section
            ></q-list
          >
        </q-card-section>
        <q-img
          class="img_main_page"
          spinner-color="primary"
          src="images/sky.jpg" /></q-card-section
    ></q-card>
    <q-card class="card" dark flat>
      <q-card-section horizontal>
        <q-img
          class="img_main_page"
          spinner-color="primary"
          src="images/bg.jpg"
        />
        <q-card-section>
          <h3>Professional Experience</h3>
          <h4>Software Engineer – Intel Corporation</h4>
          <h6>March 2022 - February 2023 (1 year)</h6>
          <h4>Technologies</h4>
          <h7
            >JavaScript, C++, CSS, HTML, .NET, React, MySQL , SSMS, ServiceNow,
            GitHub, GitLab, Docker, Postman , Jira</h7
          >
          <h4>Accomplishments</h4>
          <q-list>
            <q-item-section>
              <q-item>
                Implemented multiple data sorting modules to chart and enlist
                information for the private online tool my team worked
                on.</q-item
              >
              <q-item
                >Fixed the technical issues of hundreds of users from 7
                countries working on extensive datasets and multiple
                databases.</q-item
              >
              <q-item
                >Attended daily meetings utilizing Agile method “Scrum” through
                Jira to administrate challenging deadlines.</q-item
              >
            </q-item-section>
          </q-list>
          <q-list>
            <q-item-section>
              <q-item
                >- Frontend Developer - Ópticas Jimenez March 2023 - Present
                (Ongoing) Technologies Windows, Virtual Box, Linux, Python,
                Odoo, Postgres, MySQL, Postgres, HTML, CSS, WordPress, Elementor
                Accomplishments - Designed the landing page needed for marketing
                and enhanced the look and feel of all the sections in the
                company’s site with multiple devices in mind. - Rehabilitated
                the connection of the main private tool for storing and viewing
                web orders. - Proposed multiple improvements in the work
                environment for futureproofing in case more developers come to
                the company.</q-item
              ></q-item-section
            ></q-list
          ></q-card-section
        ></q-card-section
      >
    </q-card>
    <q-card class="card" dark flat>
      <q-card-section horizontal>
        <q-card-section>
          <h3>Technical Skills</h3>
          <q-card-section horizontal>
            <q-card-section>
              <h4>Programming Languages</h4>
              <q-list
                ><q-item-section>
                  <q-item>HTML ●●●●● </q-item>
                  <q-item>Python ●●●●● </q-item>
                  <q-item>JavaScript - .Net ●●●●● </q-item>
                  <q-item>C ●●●●○ </q-item>
                  <q-item>C++ ●●●●○ </q-item>
                  <q-item>CSS ●●●●○</q-item></q-item-section
                ></q-list
              >
              <h4>Frontend</h4>
              <q-list
                ><q-item-section>
                  <q-item>Vue - Vuetify - Quasar ●●●●● </q-item>
                  <q-item>Wordpress - Elementor ●●●●● </q-item>
                  <q-item>React ●●●●○</q-item></q-item-section
                ></q-list
              > </q-card-section
            ><q-card-section>
              <h4>Databases</h4>
              <q-list
                ><q-item-section>
                  <q-item>SQL - MySQL ●●●●● </q-item>
                  <q-item>MongoDB ●●●●○ </q-item>
                  <q-item>Firebase ●●●●○ </q-item>
                  <q-item>Engines Unity ●●●●○</q-item>
                  <q-item>Unreal Engine 5 ●●●●○ </q-item>
                  <q-item>Godot ●●○○○</q-item></q-item-section
                ></q-list
              >
              <h4>Tools</h4>
              <q-list
                ><q-item-section>
                  <q-item>Studio Code ●●●●●</q-item>
                  <q-item>GitHub ●●●●●</q-item>
                  <q-item>Office 365 & Figma ●●●●● </q-item>
                  <q-item>Postman ●●●●○ </q-item>
                  <q-item>SSMS ●●●●○ </q-item>
                  <q-item>Docker ●●●●○</q-item></q-item-section
                >
              </q-list>
            </q-card-section>
          </q-card-section>
        </q-card-section>

        <q-img
          class="img_main_page"
          spinner-color="primary"
          src="images/yo.jpg"
        /> </q-card-section
    ></q-card>
    <q-card class="card" dark flat>
      <q-card-section horizontal>
        <q-img
          class="img_main_page"
          spinner-color="primary"
          src="images/Yoshi.gif"
        />
        <q-card-section>
          <h3>Personality Traits</h3>
          <h4>Soft Skills</h4>
          Teamwork Active listening Confidence Creativity Patience Attention to
          detail Assertive communication Adaptability Proactivity
          <h4>Hobbies</h4>
          Exercise Art Gaming Music Series Hangouts</q-card-section
        ></q-card-section
      ></q-card
    >
  </q-page>
</template>
<style>
.card {
  width: 99.5%;
}
.img_main_page {
  min-width: 40%;
  max-width: 50%;
}
</style>
<script>
import NameAnim from "../components/NameAnim.vue";
import StaryBg from "../components/StaryBg.vue";
export default {
  name: "IndexPage",
  data() {
    return {
      extend: false,
    };
  },
  methods: {
    getExtend() {
      return this.extend;
    },
  },
  watch: {},
  mounted() {
    /*setInterval(OnTick, 10);

    function OnTick() {
      extend = this.getExtend();
      console.log("Is extend true?", this.extend);
    };*/
  },
  components: {
    NameAnim,
    StaryBg,
  },
};
</script>
