<template>
  <q-page class="CenturyGothic" style="overflow-x: hidden">
    <!--This section is used to animate my name-->
    <div @mouseover="extend = true" @mouseleave="extend = false">
      <h1 class="text-accent">
        Jason<NameAnim label="Piedra" :extend="extend" /><NameAnim
          label="Matamoros"
          :extend="extend"
        />
      </h1>
    </div>
    <!---->
    <div>
      <text>Frontend Developer | Software Developer</text>
      <q-card dark>
        <h3>Summary</h3>
        <q-list
          ><q-item-section
            ><q-item
              >- Dependable Frontend Developer with creative and effective
              problem solving.</q-item
            ><q-item
              >- Native Spanish speaker with excellent proficiency in English
              (C1).</q-item
            ><q-item>
              - Invested in hard work and collaboration to get accurate
              solutions efficiently.</q-item
            ><q-item>
              - Always willing to learn, be it from coworkers or
              self-studying.</q-item
            ><q-item>
              - Detail-oriented professional focused in creating intuitive and
              innovative UIs.</q-item
            >
          </q-item-section>
        </q-list>
      </q-card>
      <q-card dark>
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
        ></q-card
      ><q-card dark
        ><h3>Professional Experience</h3>
        <q-list
          ><q-item-section
            ><q-item
              >Software Engineer – Intel Corporation March 2022 - February 2023
              (1 year) Technologies JavaScript, C++, CSS, HTML, .NET, React,
              MySQL , SSMS, ServiceNow, GitHub, GitLab, Docker, Postman , Jira
              Accomplishments - Implemented multiple data sorting modules to
              chart and enlist information for the private online tool my team
              worked on. - Fixed the technical issues of hundreds of users from
              7 countries working on extensive datasets and multiple databases.
              - Attended daily meetings utilizing Agile method “Scrum” through
              Jira to administrate challenging deadlines.</q-item
            ><q-item
              >- Frontend Developer - Ópticas Jimenez March 2023 - Present
              (Ongoing) Technologies Windows, Virtual Box, Linux, Python, Odoo,
              Postgres, MySQL, Postgres, HTML, CSS, WordPress, Elementor
              Accomplishments - Designed the landing page needed for marketing
              and enhanced the look and feel of all the sections in the
              company’s site with multiple devices in mind. - Rehabilitated the
              connection of the main private tool for storing and viewing web
              orders. - Proposed multiple improvements in the work environment
              for futureproofing in case more developers come to the
              company.</q-item
            ></q-item-section
          ></q-list
        ><text>
          Technical Skills Programming Languages HTML ●●●●● Python ●●●●●
          JavaScript - .Net ●●●●● C ●●●●○ C++ ●●●●○ CSS ●●●●○ Frontend Vue -
          Vuetify - Quasar ●●●●● Wordpress - Elementor ●●●●● React ●●●●○
          Databases SQL - MySQL ●●●●● MongoDB ●●●●○ Firebase ●●●●○ Engines Unity
          ●●●●○ Unreal Engine 5 ●●●●○ Godot ●●○○○ Tools Visual Studio Code ●●●●●
          GitHub ●●●●● Office 365 & Figma ●●●●● Postman ●●●●○ SSMS ●●●●○ Docker
          ●●●●○ Personality Traits Soft Skills Teamwork Active listening
          Confidence Creativity Patience Attention to detail Assertive
          communication Adaptability Proactivity Hobbies Exercise Art Gaming
          Music Series Hangouts</text
        ></q-card
      >
    </div>
  </q-page>
</template>

<script>
import NameAnim from "../components/NameAnim.vue";
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
  },
};
</script>
