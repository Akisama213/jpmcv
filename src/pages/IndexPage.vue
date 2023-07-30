<template>
  <!--Component made for the on hover effect-->
  <StaryBg :extend="extend" />
  <q-page class="CenturyGothic" style="overflow-x: hidden; left: 1%">
    <!--This section is used to animate my name-->
    <span @mouseover="extend = true" @mouseleave="extend = false">
      <h1 class="text-accent">
        Jason<NameAnim label="Piedra" :extend="extend" />
        <NameAnim label="Matamoros" :extend="extend" />
      </h1>
      <div id="extend_notification_text" class="extend_notification">
        <h5>extend</h5>
      </div>
    </span>

    <h6>Frontend Developer | Software Developer</h6>

    <!--Information Cards-->
    <q-card class="card" flat key="crad0">
      <q-card-section class="justify-start" horizontal>
        <q-img
          class="col-7 card_img_left"
          spinner-color="primary"
          src="https://lh3.googleusercontent.com/pw/AIL4fc-v213QWWQznIvKniy-mV2ILrIuRQHOL8EjJ6mQosd85fCC59HCganqKlapbGfw6Lap7e1wgEkNFT51ah0N2FWPuhde2iZyzQFHl7j649nw02L_i5d1x9WxZ32sLJfPS0W-IJcm-2dVzPH81Q90mZDAvIIrikWsCyRa6P6E9ZKBOBK-OBHPprGsV6zbFETJ8EhR51-ybO6QrEKgz2-41vWCyV-YSyOvhbgWaTJlyj7a8Nq-RIQEDWqt5RwbVekP0R1awR8jSBFTAzADLso-pMeaojBxkcgZgR0AmYr-lCOL4G6BdAoRWkYPOwPx_8Or5NcBEMKNiWqq6e7FOMg508hzDW1q-AN2CQ8yxDkhQ2xwz6mTXizl6CKjLiw-K4lbciduFXSRZ3nghoc-dAEW8IT6UeurXAj2djuCbcWGRfT6nt4gvKsFtvJpop55IJhaoBNnNOnQHtyh1kbSluDn_1C1R-aLo6gFfIXXBasVuZb_3BiuEY9p9OIigoGbonDiRvPOpiyoRcjt0hlmbQsioz75_umnHNKSYNlZhDSiHYkQ_aFp65UfgJT7mXdtbsL7Uy4Q8pbszTAWh6xl0Rdi9Xdk6ojiGIAGp1bupXqc17XmJuqUmnQv-YmnGUAkzjG0Hom11E0q50zImIb6iPvQTo8WOwUfVqWkesb1B3O6xxeZV9LsjRa6-0kACOWZW5QvOAI3zdlZPCsDZ18aqPP7WuyV2fiEXaEEe5O8GAuqOvTHYvYbB2_Ez-sWqFqvXXZHD3YMS4mt42TX0x8zxBVbFuysKKKD7miOJlZKrD67H3gSuiNz5214oZwpKHXHKMwMENEhbvRtqXA67Z5AYo9Vw0mhtC1KE23mBKXYa1ILDSh2J3Mw_XDBTwF7hPNfjUwG0HZB72U-AJ_KidLbjRpGm13lBFh4lZJu_JubH7DxYCb56XGxcvN4yzQeUznM=w640-h640-s-no?authuser=0"
        />
        <q-card-section class="col">
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
          class="col-5"
          src="https://lh3.googleusercontent.com/pw/AIL4fc-mUSX5BdBs7pnz6wIFczUROOfbVQuArBWRu-dCDXmrKIkol4GnmeD7dYEQlRIHKR-Yc3Hu6uH4FaK3CC9KTzfxNnLR4ah5aq4h-T8TBZvkv9Iedtqq-l848p0Vc6BLSbHT0pA3Q7vV4juU02U1ga8QjWNKAszGixT-t40RGY2LwovwUIRgH1wgklP2dCNrrE5_f_zS3BIhY4Xwu71D6WQoxWoDD_Y8jjZwzs3IJdgHc-JCRve-m6KXhJ7SAM0CSIkgQ5IdRQmxC6SfW7kj5E_UzYVIfB5tBwt-6oExXpF41h-qFDgxJnkja9WzJ5tj7Ph7GFLkosji-ngtXCaqhJqsfVYIUgYZ_iOS1ffU3vI03CdwSddEzC6iey1wTmNuYRhoUOZnOqzpnJGrhJtuVwtjhHHUA-WIGlXhAxST4ACQjd-o1IObv2xU3hLsMu5R5ESjtSyaArZJRTPR9v4qaIHgJVQ3TbBdBhHJ4B9FLLvUGYlb4uH3tOTkMdkFFwsk54hS_pJmI8H6JTJY_h5T4hNB5xF33gi7hl3KTQ_VbPFv4AzjaWdQKwSO83Dzktclv0OUA2rJ-hWSl37ZV6V56LMsTrw8ksd10M0zuv3JYujrzq-yhPfobl6lz4HeAoB7SQPDlRsvYCralY1_s1uCBQnQ_LVgnhrx4hK6KPzHR9YEkIc6YQpqtXXcMnAt08mn69alr3fNqxjtcZulutt7AaGSilY-ybm9suhsHnDSYz3VVGrEebgbDZj7iHiidlFAtxAzWoKUqk4qlc9PLnv598GQRqmwcW5ZqUOZR5oMMLaeVIHvlYqanaIAx5q3FXh11xxoqXV9n3OS6a74kugI_2z084MUkiYUhJl8-evUUhJ3P02ZxHR0ELbC5zp0QAi2JiWERH08XaoEKrgGmzrx8a3bJevF31EEk7KgT5wWAYHl-52RHPpRDrhHgHK5=w567-h567-s-no?authuser=0"
          spinner-color="primary"
        />
      </q-card-section>
    </q-card>
    <q-card class="card" dark flat>
      <q-card-section class="justify-start" horizontal>
        <q-img
          class="col-5"
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
          class="col-5"
          spinner-color="primary"
          src="https://lh3.googleusercontent.com/pw/AIL4fc9zLpKOr_RbKw8SN8cigg-GnKU6rK_xbrRihyBh1sasHQZ-X5VWv399tdK-P37U9iY-S8i_KhQTGGHmp1EpxcsaGo9I5kggHCt00d5bs_43wb2TkqfwypoSzDcUQrgfp82KnZH4e_D4GSegtwrlEtvj25rRNyZ2S04srFB3-WSQ96xZSvloKarL2TEvsUJf1LTienuGqxrShRyHdY0v2w9ceYWVD2EVGMX346o5CLngUI4YibJWGtbdgPMyysAHvQ10tXkOHP3dp7KGuJmOfj01bhtZG9hKp4HQBJkML0yu4mxzPB8fBgScz1NeTUP8MiKrwifPrSm_6Ecgn0Y2JRIzfgoLfOgJ2JrV3670nCZ2RgHqz0dQNMkmZyuI3BiRLko5BnKIPYukWKRFKy2q6gI4iRR-mY4U-JFP59SnWV2pUK8w_u7F7w24Vt6K2neLcG2Kimg53Uhp015Qkjk7DfVukn1FLEVEe3rYVarlNLnMHPKOdzkmnPSLXUXqL2bSC0bGKSyPZJA8POT8Cpzx_vw-KAOTewwCgmOyO-uxiA3mdp5VnrBtoLU3WgJK3s092KPkwnG8t2AR9G8aDPQu4IPrvwTWNeUm54MQHU9Wfln2C3na7c7UrGd9U9Qm0Ut8lIC_qMVjktldBoV4EELvMg68YvFzlcpFOa5CljgSdGvxogwy-nM51oI6BLTc2T4P9cN6XzQ3Fd338VA62HPzIyQG_nNW-PevB-8SxKm4O4B5wEzPTOuQgctnhUkYdM8YUK8n77oa6HeOEfs3NFcosAVkuyioLrbAmyyLfDmA9dc-aVzLwyLMXNM7_iFXBbpkrlRSzKfoO46sCJZt-XQFH5osbY5sYiZT7zdy5ZF9lk_U7sn7nJYKslqR4Q2xKxxxVWoFQVuRH6LGbBuQoVRKPDocShAi4-BR3XtSBx98ERiBMaa95KNYR-0o0cbY=w540-h405-s-no?authuser=0"
      /></q-card-section>
    </q-card>
  </q-page>
</template>
<style>
.card {
  max-height: 80vh;
  width: 98%;
  background-color: rgba(#2c1b2c, 0.5);
}
.card_img_left {
  display: block;
  width: 100%;
  mask-image: linear-gradient(to right, black, transparent 95%);
  mask-mode: alpha;
}
.card_img_right {
  display: block;
  width: 100%;
  mask-image: linear-gradient(to right, black, transparent 95%);
  mask-mode: alpha;
}
.extend_notification {
  rotate: 2deg;
  top: 0.5%;
  left: 19%;
  position: absolute;
  opacity: 50%;
}
.move_away {
  transition: all 1s ease;
  opacity: 0%;
  left: 22%;
  top: -1%;
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
