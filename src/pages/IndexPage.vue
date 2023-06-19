<template>
  <q-page class="CenturyGothic" style="overflow-x: hidden">
    <StaryBg :extend="extend" />
    <!--This section is used to animate my name-->
    <span @mouseover="extend = true" @mouseleave="extend = false">
      <h1 class="text-accent">
        Jason<NameAnim label="Piedra" :extend="extend" />
        <NameAnim label="Matamoros" :extend="extend" />
      </h1>
    </span>
    <h6>Frontend Developer | Software Developer</h6>

    <q-card dark flat key="crad0">
      <q-card-section horizontal>
        <q-img key="image0" src="src\assets\images\rose.jpg" scale-down />
        <q-card-section key="textSection0">
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
    <q-card dark flat>
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
          ></q-card-section
        >
        <q-img
          src="src\assets\images\lincoln.jpg"
          fit="contain" /></q-card-section
    ></q-card>
    <q-card dark flat>
      <q-card-section horizontal>
        <q-img key="image0" src="src\assets\images\bg.jpg" fit="contain" />
        <q-card-section>
          <h3>Professional Experience</h3>
          <q-list
            ><q-item-section
              ><q-item
                >Software Engineer – Intel Corporation March 2022 - February
                2023 (1 year) Technologies JavaScript, C++, CSS, HTML, .NET,
                React, MySQL , SSMS, ServiceNow, GitHub, GitLab, Docker, Postman
                , Jira Accomplishments - Implemented multiple data sorting
                modules to chart and enlist information for the private online
                tool my team worked on. - Fixed the technical issues of hundreds
                of users from 7 countries working on extensive datasets and
                multiple databases. - Attended daily meetings utilizing Agile
                method “Scrum” through Jira to administrate challenging
                deadlines.</q-item
              ><q-item
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
      ></q-card
    >
    <q-card dark flat>
      <q-card-section horizontal>
        <q-card-section>
          <h3>Technical Skills</h3>
          <h4>Programming Languages</h4>
          HTML ●●●●● Python ●●●●● JavaScript - .Net ●●●●● C ●●●●○ C++ ●●●●○ CSS
          ●●●●○
          <h4>Frontend</h4>
          Vue - Vuetify - Quasar ●●●●● Wordpress - Elementor ●●●●● React ●●●●○
          <h4>Databases</h4>
          SQL - MySQL ●●●●● MongoDB ●●●●○ Firebase ●●●●○ Engines Unity ●●●●○
          Unreal Engine 5 ●●●●○ Godot ●●○○○
          <h4>Tools</h4>
          Visual Studio Code ●●●●● GitHub ●●●●● Office 365 & Figma ●●●●● Postman
          ●●●●○ SSMS ●●●●○ Docker ●●●●○</q-card-section
        ><q-img src="src\assets\images\yo.jpg" /></q-card-section
    ></q-card>
    <q-card dark flat>
      <q-card-section horizontal>
        <q-img key="image0" src="src\assets\images\Yoshi.gif" />
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
