<template>
  <!--Component made for the on hover effect-->
  <StaryBg :extend="extend" />
  <q-page style="left: 1%">
    <!--This section is used to animate my name-->
    <div>
      <h1
        style="display: inline-block"
        @mouseover="extend = true"
        @mouseleave="extend = false"
        class="text-accent"
      >
        Jason<NameAnim label="Piedra" :extend="extend" />
        <NameAnim
          style="clear: both; float: left"
          label="Matamoros"
          :extend="extend"
        />
      </h1>
      <div id="extend_notification_text" class="extend_notification">
        <h4>hover</h4>
      </div>
    </div>

    <h6>Frontend Developer | Software Developer</h6>

    <!--Information Cards-->
    <q-card class="card" dark flat>
      <q-card-section class="justify-start" horizontal>
        <q-img
          class="col-5 card_img_left"
          spinner-color="primary"
          src="https://lh3.googleusercontent.com/pw/AIL4fc-v213QWWQznIvKniy-mV2ILrIuRQHOL8EjJ6mQosd85fCC59HCganqKlapbGfw6Lap7e1wgEkNFT51ah0N2FWPuhde2iZyzQFHl7j649nw02L_i5d1x9WxZ32sLJfPS0W-IJcm-2dVzPH81Q90mZDAvIIrikWsCyRa6P6E9ZKBOBK-OBHPprGsV6zbFETJ8EhR51-ybO6QrEKgz2-41vWCyV-YSyOvhbgWaTJlyj7a8Nq-RIQEDWqt5RwbVekP0R1awR8jSBFTAzADLso-pMeaojBxkcgZgR0AmYr-lCOL4G6BdAoRWkYPOwPx_8Or5NcBEMKNiWqq6e7FOMg508hzDW1q-AN2CQ8yxDkhQ2xwz6mTXizl6CKjLiw-K4lbciduFXSRZ3nghoc-dAEW8IT6UeurXAj2djuCbcWGRfT6nt4gvKsFtvJpop55IJhaoBNnNOnQHtyh1kbSluDn_1C1R-aLo6gFfIXXBasVuZb_3BiuEY9p9OIigoGbonDiRvPOpiyoRcjt0hlmbQsioz75_umnHNKSYNlZhDSiHYkQ_aFp65UfgJT7mXdtbsL7Uy4Q8pbszTAWh6xl0Rdi9Xdk6ojiGIAGp1bupXqc17XmJuqUmnQv-YmnGUAkzjG0Hom11E0q50zImIb6iPvQTo8WOwUfVqWkesb1B3O6xxeZV9LsjRa6-0kACOWZW5QvOAI3zdlZPCsDZ18aqPP7WuyV2fiEXaEEe5O8GAuqOvTHYvYbB2_Ez-sWqFqvXXZHD3YMS4mt42TX0x8zxBVbFuysKKKD7miOJlZKrD67H3gSuiNz5214oZwpKHXHKMwMENEhbvRtqXA67Z5AYo9Vw0mhtC1KE23mBKXYa1ILDSh2J3Mw_XDBTwF7hPNfjUwG0HZB72U-AJ_KidLbjRpGm13lBFh4lZJu_JubH7DxYCb56XGxcvN4yzQeUznM=w640-h640-s-no?authuser=0"
        />
        <q-card-section class="col">
          <h3>About</h3>
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
          <h3>Education</h3>
          <q-list
            ><q-item-section
              ><h5>High School Diploma - Conversational English Diploma</h5>
              <q-item> Liceo Experimental Bilingüe 2014 - 2019</q-item>
              <h5>Bachelor’s Degree in Computer Engineering</h5>
              <q-item>
                Tecnológico de Costa Rica 2020 - 2024
              </q-item></q-item-section
            ></q-list
          >
        </q-card-section>
      </q-card-section>
    </q-card>
    <q-card class="card" dark flat>
      <q-card-section class="justify-end" horizontal>
        <q-card-section class="col">
          <h3>Professional Experience</h3>
          <h4>Software Engineer – Intel Corporation</h4>
          <h6>March 2022 - February 2023 (1 year)</h6>
          <h4>Technologies</h4>
          <sub
            >JavaScript, C++, CSS, HTML, .NET, React, MySQL , SSMS, ServiceNow,
            GitHub, GitLab, Docker, Postman, Jira</sub
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
        >
        <q-img
          class="col-7 card_img_right"
          src="https://lh3.googleusercontent.com/pw/AIL4fc92oahFFdyWezVmaBUK9sGprGj5NA-EEUk8Y333DvyXn5pUug3IRECz92RiPdhJ-p67VeT79_qO8MmLxW1wMDbCgf8f0ltmKGyXRwe41cdH_QSKiN-QWZve7pcfQnQNN7MWKWHBadEeGSspOP5yvU3OwT_quC_GCLuFYZHQFdtiSiA6zI1XQgSHedE6eNnscxbsIs8-RXv4tCyvClRqEEFRmDBkHkNutri1yzZO5bUMPpg0EF9rM3eW4dGzUsmRmpVQdo8ilEu_gbf7DiPVha-kt1mPlkH2ZEakjs_xPf6uGEi8ux3s8pC1onilhbBydHu7_KPQm_VM8ylafmSEgpNL6fiiZVKQQHFF2OqVmqnp16FqxqbByfa8epSmOBm8RxoQTjI6f2_DYeFnoCpRBZNl76dvpFjIGMpGq0OW2YB6qiM6SmmmBQFOBQNxcNjb9Iaul8J8Rr8EdDzE7WLntH88uRWIz3Lv-YfgAku17Z4ZE_PhEttBbYQyJ-dO7FRO0yfxW_wOhWGVBIWvMmFR1Rg5EXwjRqv_w4E2IaQvkcWBWIvPz_6HTBLX9DDcysA8XxmrPfj_0vszPZgenyE4XYq6MpV6CvnmodAaejympKWAJmR11otfHi1jk0WPVnAFgwpZI0HzN2Nght3-IERMsOybJvjDP9x8sbF5jcM02KVJUAYCf9Q9VTXYi1zG4jqdfPedgdlmRICdQd3w-RNxza5fnlp8MjovyaO4htUE1hWVm4UkYpZe8kfMp6zZbcxCA6Amx2U1f9RoRgQEUqroRga3fEeIPhoQYZwcsUO9tzdvLZZ_wyy-oROZbOeRPwxlLY906bUwkC-o8hvtfFoIE2GlXeX2k2j9F0YsTHoAliWtFgltEQaV9QQ7NETrMJWqQ5kVms6GNG3AVVhW0eIr9Qbs84XWUlK3FOlJtH0zppEW9eSKU9T9ZnUyIh62=w1008-h567-s-no?authuser=0"
          spinner-color="primary"
        />
      </q-card-section>
    </q-card>
    <q-card class="card" dark flat>
      <q-card-section class="justify-start" horizontal>
        <q-img
          class="col-5 card_img_left"
          src="https://lh3.googleusercontent.com/pw/AIL4fc_O4dObW-aDgDHiZ8arZMPLNae_fBFApbI_7OI7gNNygZ5vMAQYxB2odNR2pJxI1GHYRMPcnHU1vfcUrNrCdQnFoHuT5oN2xfJA8tX-R9NRotADJ7IOmXONELWrSdN9fcRBm7kW4AxRTWPRLYd1YR2nW1bHOf6ErwTf2SQhJC0Caid4Na2SXEdGPovre5Fql0sFMTJdHX6KGhX8-KdCfumRet1fyYTDluMS9_1HKskRInlqJtjhctHKNetrRsmD7jyWeYw00icoLKEbBkMQO48BFXShOc-dlw2VKcZHj-1J14Q_cY9B6U5rlhrXj46i5dvKMwuRymcWkhna3aIxhiFrG2Q83Wi3b0d0ZEnE10fVnkx1CXjXB6qKNVQmvflfB39mM9zVXwiEz64oPC-YL962sn4x5YO4K_3QBMe_pudtJAxYelVnp7NL-hIoYPUvzj_rNm63xCZnpSh2B2MBVBhaAWR3WvReaierVLv_0nA-d0WUFyvq2BHEqntZmtzqGtk9rrGX3Ayhq2TqshwchSztDtHTtMM5i8Vde0ozxbZrqX3iXhKr9dKx0RRYZOlm7rm6crhTT-bTvC8Xe6r6TOLTuNhU6MSsjejsLx-huaG5T_K80tz-q2Qr33z4SOQfRStzC9PwCmqm9nuB7hJVfeIttXJFz85WxNBgMNkIqvHaJJ8vnakHYDsy6NOGyYjknDxyi1f4PUNsB0-Nl8EG-TIjbg6h4i-Nf035TSP0EIS3JEyaglLWAhNZpcwKXwfeVtqRv-efMEhM8JknmQ_oYYCtoyuHBqyV06-LTrBKRXP6bghu4tP5e8v-XbTH8WQredxBk5EzAwUUk-d1turRk3Houg-aFIm67GjdNnG5Stuu4NXPZX2SZ6BD34gfpz-oBYSRMSK1OAmw2PF6TwmxxlnS8SBYFAiD8dTo7CCmahJVTqLLy__y1wP_V3T0=w801-h1001-s-no?authuser=0"
          spinner-color="primary"
        />
        <q-card-section class="col">
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
      </q-card-section></q-card
    >
    <q-card class="card" dark flat>
      <q-card-section class="justify-end" horizontal>
        <q-card-section class="col">
          <h3>Personality Traits</h3>
          <h4>Soft Skills</h4>
          Teamwork Active listening Confidence Creativity Patience Attention to
          detail Assertive communication Adaptability Proactivity
          <h4>Hobbies</h4>
          Exercise Art Gaming Music Series Hangouts</q-card-section
        >
        <q-img
          class="col-7 card_img_right"
          spinner-color="primary"
          src="https://photos.app.goo.gl/KseJWCnry6pfZgSH6"
      /></q-card-section>
    </q-card>
  </q-page>
</template>
<style>
.card {
  max-height: 85vh;
  width: 98%;
  background-color: rgba(#2c1b2c, 0.5);
  overflow-y: scroll;
}
.card_img_left {
  display: block;
  max-height: 85vh;
  width: 100%;
  mask-image: linear-gradient(to right, black, transparent 95%);
  mask-mode: alpha;
}
.card_img_right {
  display: block;
  max-height: 85vh;
  width: 100%;
  mask-image: linear-gradient(to left, black, transparent 95%);
  mask-mode: alpha;
}
.extend_notification {
  background: url(https://lh3.googleusercontent.com/pw/AIL4fc_TxjQ0xklrDRNmaitEcCilP6XFsjWgcd4ct7bbHnsr_PZ3_3Qp5dUtN-TseX06jjAObNAdN4dLznPyn4VZk7e6gjBLjNkEY8_B2gyofMcIF7mH_vMJLFvjn7yUY9v3lPWAItTsLOodDBUWH5HQM6HWMqYX4RRaAwMo5NSKjyLUcSWU8OOtFb0PZRzOmfpRboKuGUYMNIxH8vq2MajcwWmyz19zHZhyk6GpGLBtQvXX24ifyJtjzBM25lZG3IkLE214vvNXxmcddR6PZNN6oROJyxRqgy7ZP5C5O14JD5EYqAjS1kaxhFKi_As4pvphewg3eEAK-i9ZWkkq_zea-BMDmXPPJRwtQTTptOmkovM8uljYxiXoLqS2TG2fkgrEzciyoR6Numq4YRjNOxnLTfZ7csadmq78k0eXiqEyIHZIWLjLux3EJQciAZhfrtX1O7ho3Kr91EoYVS6ulmOjbsEW7ST4lpc9tttLD6u5cjeXNhxwlyrWSH4tEE6UHQDpA0kgjOC4tk8_yK30sYtQS4U4FH7XfOZhIUChzT_dxHgx9TBYNdaEkDuc_nzwU2kAEMbEScZM02wkDH-Mh84tyPLCe_aoDcWzO4i61wSakwI17XQCz2vhWzWm0WavZH26-uqsfjYwR0nuQ627YpfQX8llBh06LzQlgcV47gMM6oy5LZ_HWQ_RWiJVb7RFBjrcCuh8wzYoyYDj-Bhwa2CYlIjqx6L3Wo_jltR8SFrDiGbND1U03ljcmob2LSxtw9S-tu2_XUDW_d07PZUSGKBlPyyVnqLaRL6-KEw84LGJnStwJZfaYraa1Bp2-xJu9-1jMC0qTlQmDKwgSKr1cBKOFolebjRKtG4YEnMp3pBbOKgfj6Z2VJkgT0vjYHn5ApDjvskInAa4prDU6gfKtx8m-MXwrrNroJoIfUHCwE6YJ-mwtFOln7CvOtZByQcz=w462-h346-no?authuser=0)
    0 0 / cover no-repeat;
  -webkit-text-fill-color: transparent;
  -webkit-background-clip: text;
  background-clip: text;
  rotate: 2deg;
  top: 0.5vh;
  left: 22vw;
  position: absolute;
  opacity: 90%;
}
.move_away {
  rotate: -50deg;
  transition: rotate 1.5s ease-out, opacity 0.8s ease, left 1.1s ease-out,
    top 0.6s;
  opacity: 0%;
  left: 28vw;
  top: -2vh;
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
  watch: {
    extend(val) {
      if (val) {
        const div = document.getElementById("extend_notification_text");
        div.classList.add("move_away");
      }
    },
  },
  components: {
    NameAnim,
    StaryBg,
  },
};
</script>
