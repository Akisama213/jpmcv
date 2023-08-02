<template>
  <!--Component made for the on hover effect-->
  <div id="Stary">
    <StaryBg :extend="extend" />
  </div>
  <q-page id="Main_Page">
    <!--This section is used to animate my name-->
    <div style="margin-left: 1em">
      <div id="JasonPM" style="display: flex">
        <h1
          @mouseover="extend = true"
          @mouseleave="extend = false"
          class="text-accent"
          style="
            width: fit-content;
            height: fit-content;
            display: inline-block;
            margin-top: 0.3em;
            margin-bottom: 0.2em;
          "
        >
          Jason<NameAnim label="Piedra" :extend="extend" />
          <NameAnim label="Matamoros" :extend="extend" />
        </h1>
        <div id="extend_notification_text" class="extend_notification">
          <h4>hover</h4>
        </div>
      </div>

      <h6 id="Subtitle">Frontend Developer | Software Developer</h6>
    </div>
    <div id="Scroll" class="scroll_section">
      <div class="shape">
        <div
          @click="card_menu()"
          id="scrollText"
          style="position: absolute; transform: translate(-50%, -50%)"
        >
          <svg
            id="rotatingText"
            preserve-aspect-ratio="true"
            viewBox="0 0 200 200"
            width="40vmax"
            height="40vmax"
          >
            <defs>
              <path
                id="circle"
                d="M 100 100
                m -50, 0
                a 50, 50 0 1, 1 100, 0
                a 50, 50 0 1, 1 -100, 0 Z
                "
              ></path>
            </defs>
            <text>
              <textPath
                class="text"
                style="font-weight: 600; letter-spacing: 1.7px; font-size: 19"
                alignment-baseline="top"
                xlink:href="#circle"
              >
                scroll scroll scroll scroll scroll
              </textPath>
            </text>
          </svg>
        </div>
      </div>
    </div>
    <!--Information Cards-->
    <div
      id="Cards"
      class="row no-wrap absolute-center"
      style="width: max-content; overflow-x: auto; transform: translateY(100%)"
    >
      <q-card class="card q-mx-xl" dark flat>
        <q-card-section class="justify-start" horizontal>
          <q-img
            class="col-5 card_img_left"
            spinner-color="primary"
            src="https://lh3.googleusercontent.com/pw/AIL4fc8Nb2Bhg-eiIk4ZmweNPjSdaGAomwVS5WPgeS4JR1ZhfJZISRVTo_IiOxJkcaeC3MweE6JUz8iu9EqGixI8tSEOQfbinW310ScTXg3zcRhLovPjIsY0=w2400"
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
                  >Detail-oriented professional focused in creating intuitive
                  and innovative UIs.</q-item
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
      <q-card class="card q-mx-xl" dark flat>
        <q-card-section class="justify-end" horizontal>
          <q-card-section class="col">
            <h3>Professional Experience</h3>
            <h4>Software Engineer – Intel Corporation</h4>
            <h6>March 2022 - February 2023 (1 year)</h6>
            <h4>Technologies</h4>
            <sub
              >JavaScript, C++, CSS, HTML, .NET, React, MySQL , SSMS,
              ServiceNow, GitHub, GitLab, Docker, Postman, Jira</sub
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
                  >Attended daily meetings utilizing Agile method “Scrum”
                  through Jira to administrate challenging deadlines.</q-item
                >
              </q-item-section>
            </q-list>
            <q-list>
              <q-item-section>
                <q-item
                  >- Frontend Developer - Ópticas Jimenez March 2023 - Present
                  (Ongoing) Technologies Windows, Virtual Box, Linux, Python,
                  Odoo, Postgres, MySQL, Postgres, HTML, CSS, WordPress,
                  Elementor Accomplishments - Designed the landing page needed
                  for marketing and enhanced the look and feel of all the
                  sections in the company’s site with multiple devices in mind.
                  - Rehabilitated the connection of the main private tool for
                  storing and viewing web orders. - Proposed multiple
                  improvements in the work environment for futureproofing in
                  case more developers come to the company.</q-item
                ></q-item-section
              ></q-list
            ></q-card-section
          >
          <q-img
            class="col-7 card_img_right"
            src="https://lh3.googleusercontent.com/pw/AIL4fc-RUC6_8H2n1pdL_G14lnqRmTY7jpPCjnwZUUCwBhEwhKzE6SKOUD2ToPC9i-xVmYtZt-NAalHK_OaryXzPy6xR6fY-F8MjFfIT5CZ9Bacm3_39Fbqv=w2400"
            spinner-color="primary"
          />
        </q-card-section>
      </q-card>
      <q-card class="card q-mx-xl" dark flat>
        <q-card-section class="justify-start" horizontal>
          <q-img
            class="col-5 card_img_left"
            src="https://lh3.googleusercontent.com/pw/AIL4fc-L2Ws535Y1Ejwkjxjrh7sZ_5Wef3y4dI5DhHuMkZOebNgAHujn3UCHUUqsJckSH36LzyRfikkSb1mJMS7q8jq4UXsQgfu4MrZh6N8F3cFPnNzuT17J=w2400"
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
      <q-card class="card q-mx-xl" dark flat>
        <q-card-section class="justify-end" horizontal>
          <q-card-section class="col">
            <h3>Personality Traits</h3>
            <h4>Soft Skills</h4>
            Teamwork Active listening Confidence Creativity Patience Attention
            to detail Assertive communication Adaptability Proactivity
            <h4>Hobbies</h4>
            Exercise Art Gaming Music Series Hangouts</q-card-section
          >
          <q-img
            class="col-7 card_img_right"
            spinner-color="primary"
            src="https://lh3.googleusercontent.com/pw/AIL4fc_ezoU5_WugYaOamdGG4iCfR66wmoK-EDrNJyytxytf88Al8BrWVcLSsqdBuOOJSDPMEA_G_eIDw_EO3Jj-uC5x4XFYd6G18JoGtkwWS1IAox4zMNoY=w2400"
        /></q-card-section>
      </q-card>
    </div>
  </q-page>
</template>
<style>
#scrollText {
  mask-image: linear-gradient(black 50%, transparent 55%);
  mask-mode: alpha;
  opacity: 50%;
}
#rotatingText {
  animation: rotation 15s infinite linear;
}
@keyframes rotation {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(359deg);
  }
}
.shape {
  content: "scroll";
  position: absolute;
  opacity: 40%;
  left: 50vw;
  top: 90vh;
  width: 0vmax;
  height: 0vmax;
  transform: translate(-50%, -50%);
  border-right: 1vmax solid transparent;
  border-top: 1vmax solid black;
  border-left: 1vmax solid transparent;
  border-top-left-radius: 10vmax;
  border-top-right-radius: 10vmax;
  margin: 0 auto;
  display: inline-block;
  animation: arrow 3s ease infinite;
}
.shape::before {
  content: "";
  width: 15vmax;
  height: 15vmax;
  position: absolute;
  transform: translate(-50%, -50%);
  left: 50%;
  top: 50%;
  border-right: 1vmax solid transparent;
  border-top: 1vmax solid black;
  border-left: 1vmax solid transparent;
  border-top-left-radius: 20vmax;
  border-top-right-radius: 20vmax;
  margin: 0 auto;
  animation: arrow-part 3s infinite;
  animation-delay: 1.5s;
}
.shape::after {
  content: "";
  width: 30vmax;
  height: 30vmax;
  position: absolute;
  transform: translate(-50%, -50%);
  left: 50%;
  top: 50%;
  border-right: 1vmax solid transparent;
  border-top: 1vmax solid black;
  border-left: 1vmax solid transparent;
  border-top-left-radius: 20vmax;
  border-top-right-radius: 20vmax;
  margin: 0 auto;
  animation: arrow-part 3s infinite;
}
@keyframes arrow {
  0% {
    transform: translate(-50%, -50%);
    border-right: 1vmax solid transparent;
    border-top: 1vmax solid black;
    border-left: 1vmax solid transparent;
  }
  20% {
    transform: translate(-50%, 50%);
    border-right: 1.5vmax solid transparent;
    border-top: 1.5vmax solid black;
    border-left: 1.5vmax solid transparent;
  }
  30% {
    transform: translate(-50%, 20%);
    border-right: 1vmax solid transparent;
    border-top: 1vmax solid black;
    border-left: 1vmax solid transparent;
  }
  40% {
    transform: translate(-50%, 50%);
    border-right: 1.5vmax solid transparent;
    border-top: 1.5vmax solid black;
    border-left: 1.5vmax solid transparent;
  }
  100% {
    transform: translate(-50%, -50%);
    border-top: vmax solid black;
    border-right: 1vmax solid transparent;
    border-top: 1vmax solid black;
    border-left: 1vmax solid transparent;
  }
}
@keyframes arrow-part {
  0% {
    width: 8vmax;
    height: 8vmax;
    border-right: 0vmax solid transparent;
    border-top: 0vmax solid black;
    border-left: 0vmax solid transparent;
  }
  15% {
    width: 8vmax;
    height: 8vmax;
    border-right: 1vmax solid transparent;
    border-top: 1vmax solid black;
    border-left: 1vmax solid transparent;
  }
  70% {
    width: 5.25vmax;
    height: 5.25vmax;
    border-right: 1vmax solid transparent;
    border-top: 1vmax solid black;
    border-left: 1vmax solid transparent;
  }
  90% {
    width: 2vmax;
    height: 2vmax;
    border-right: 1vmax solid transparent;
    border-top: 1vmax solid black;
    border-left: 1vmax solid transparent;
  }
  100% {
    width: 2vmax;
    height: 2vmax;
    border-right: 0vmax solid transparent;
    border-top: 0vmax solid black;
    border-left: 0vmax solid transparent;
  }
}
.card {
  height: 80vh;
  width: 90vw;
  background-color: rgba(#2c1b2c, 0.5);
  overflow-y: hidden;
}
.card_img_left {
  display: block;
  height: 85vh;
  mask-image: linear-gradient(to right, black, transparent 95%);
  mask-mode: alpha;
}
.card_img_right {
  display: block;
  height: 85vh;
  mask-image: linear-gradient(to left, black, transparent 95%);
  mask-mode: alpha;
}
.extend_notification {
  background: url(https://lh3.googleusercontent.com/pw/AIL4fc8ySvDJoYzhwzrfxuzUNiG_UTGM7toIvoAcBIVmHlXHI0L4fz3A0qobWHAFCOITwU9WwJKsz8puFsRUG82TZ3wBEO7UXxSWSRgFy4CAyL1r0S-vzrRz=w2400)
    0 0 / cover no-repeat;
  background-size: 600%;
  -webkit-text-fill-color: transparent;
  -webkit-background-clip: text;
  top: 2em;
  rotate: 16deg;
  left: 25.5em;
  position: absolute;
  opacity: 90%;
  animation: float 2s ease-in-out infinite;
}
@keyframes float {
  0% {
    transform: translateY(0vmax) rotate(16deg);
  }
  50% {
    transform: translateY(-0.2vmax) rotate(20deg);
  }
  100% {
    transform: translateY(0vmax) rotate(16deg);
  }
}
.move_away {
  transition: rotate 2s ease, top 1.5s ease, left 1s ease, opacity 0.6s ease;
  rotate: -100deg;
  top: -2.5vmax;
  left: 35vmax;
  opacity: 0%;
}
.scroll_section {
  opacity: 0;
}
.visible_scroll {
  transition: opacity 3s;
  transition-delay: 1s;
  opacity: 1;
}
.show_cards_a {
  position: absolute;
  opacity: 0;
  transition: all 2s ease-out;
  top: 0vh;
}
.show_cards_b {
  opacity: 1;
  transition: all 2s ease-out;
  transform: rotate(0);
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
  created() {
    this.unwatch = this.$watch("extend", (val) => {
      if (val) {
        const hover = document.getElementById("extend_notification_text");
        hover.classList.add("move_away");
        const scroll = document.getElementById("Scroll");
        scroll.classList.add("visible_scroll");
        this.unwatch();
      }
    });

    onwheel = (mouse) => {
      console.log(mouse.deltaY);
      this.scroll = mouse.deltaY;
    };
  },
  methods: {
    card_menu() {
      let element = document.getElementById("Stary");
      element.classList.add("show_cards_a");
      element = document.getElementById("JasonPM");
      element.classList.add("show_cards_a");
      element = document.getElementById("Scroll");
      element.classList.add("show_cards_a");
      element = document.getElementById("Subtitle");
      element.classList.add("show_cards_a");
      element = document.getElementById("Cards");
      element.classList.add("show_cards_b");
    },
  },
  components: {
    NameAnim,
    StaryBg,
  },
};
</script>
