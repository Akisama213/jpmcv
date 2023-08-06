<template>
  <q-page id="Main_Page">
    <div id="Opener" style="transition: all 2s">
      <!--Component made for the on hover effect-->
      <StaryBg :extend="extend" />
      <div style="margin-left: 1em">
        <!--This section is used to animate my name-->
        <div style="display: flex">
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

        <h6>Frontend Developer | Software Developer</h6>
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
                  style="
                    font-weight: 600;
                    letter-spacing: 1.7px;
                    font-size: 18;
                    opacity: 50%;
                  "
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
    </div>

    <!--Information Cards-->
    <div
      id="Cards"
      class="row no-wrap show_cards_b"
      style="
        overflow-x: hidden;
        overflow-y: hidden;
        bottom: 10vh;
        left: 10vw;
        position: absolute;
        transition: all 2s;
        width: max-content;
      "
    >
      <q-card id="card_1" class="column card q-mr-xl" flat>
        <q-img
          loading="lazy"
          style="ratio: 1; opacity: 30%; height: 80vmin; width: 80vmin"
          spinner-color="rgba(1, 1, 1, 0.5)"
          src="https://lh3.googleusercontent.com/pw/AIL4fc8Nb2Bhg-eiIk4ZmweNPjSdaGAomwVS5WPgeS4JR1ZhfJZISRVTo_IiOxJkcaeC3MweE6JUz8iu9EqGixI8tSEOQfbinW310ScTXg3zcRhLovPjIsY0=w2400"
        />
        <q-scroll-area class="cardText">
          <div style="padding-left: 2%; padding-right: 2%">
            <text>
              <h3>About</h3>
              <b>+ Dependable Frontend Developer</b> with creative and effective
              <b>problem solving.</b> <br /><br />
              <b>+</b> Native Spanish speaker with excellent proficiency in
              <b>English (C1)</b>. <br /><br />
              <b>+</b> Invested in hard work and <b>collaboration</b> to get
              accurate solutions efficiently. <br /><br />
              <b>+</b> Always <b>willing to learn</b>, be it from coworkers or
              self-studying. <br /><br />
              <b>+</b> Detail-oriented professional focused in creating
              <b>intuitive and innovative UIs</b>. <br />
              <br />
              <h3>Education</h3>
              <b>Liceo Experimental Bilingüe</b> <br />2014 - 2019
              <br />
              <br />
              <b>+</b> High School Diploma
              <br />
              <b>+</b> Conversational English Diploma
              <br />
              <br />
              <br />
              <b>Tecnológico de Costa Rica </b><br />
              2020 - 2025
              <br />
              <br />
              <b>+</b> Bachelor's Degree in <b>Computer Engineering</b>
            </text>
          </div>
        </q-scroll-area>
      </q-card>

      <q-card id="card_2" class="column card q-mx-xl" flat>
        <q-img
          loading="lazy"
          style="ratio: 1; opacity: 30%; height: 80vmin; width: 80vmin"
          spinner-color="rgba(1, 1, 1, 0.5)"
          src="https://lh3.googleusercontent.com/pw/AIL4fc-RUC6_8H2n1pdL_G14lnqRmTY7jpPCjnwZUUCwBhEwhKzE6SKOUD2ToPC9i-xVmYtZt-NAalHK_OaryXzPy6xR6fY-F8MjFfIT5CZ9Bacm3_39Fbqv=w2400"
        />
        <q-scroll-area class="cardText">
          <div style="padding-left: 2%; padding-right: 2%">
            <text
              ><h3>Professional Experience</h3>
              <h5>Software Engineer - Intel Corporation</h5>
              March 2022 - February 2023
              <br />
              <b>Technologies</b>
              <br />
              <sub
                >JavaScript, C++, CSS, HTML, .NET, React, MySQL , SSMS,
                ServiceNow, GitHub, GitLab, Docker, Postman, Jira</sub
              >
              <br />
              <b>Accomplishments</b>
              <br />
              <b>+</b> Implemented multiple data sorting modules to chart and
              enlist information for the private online tool my team worked
              on.<br />
              <b>+</b> Fixed the technical issues of hundreds of users from 7
              countries working on extensive datasets and multiple databases.<br />
              <b>+</b> Attended daily meetings utilizing Agile method “Scrum”
              through Jira to administrate challenging deadlines.<br />
              <br />
              <h5>Frontend Developer - Ópticas Jimenez</h5>
              <br />
              March 2023 - July 2023<br />
              <b>Technologies</b> <br /><sub
                >Windows, Virtual Box, Linux, Python, Odoo, Postgres, MySQL,
                Postgres, HTML, CSS, WordPress, Elementor<br
              /></sub>
              <b>Accomplishments</b><br />
              <b>+</b> Designed the landing page needed for marketing and
              enhanced the look and feel of all the sections in the company's
              site with multiple devices in mind. <br />
              <b>+</b> Rehabilitated the connection of the main private tool for
              storing and viewing web orders. <br /><b>+</b> Proposed multiple
              improvements in the work environment for futureproofing in case
              more developers come to the company.
            </text>
          </div>
        </q-scroll-area>
      </q-card>
      <q-card id="card_3" class="column card q-mx-xl" flat>
        <q-img
          loading="lazy"
          style="ratio: 1; opacity: 40%; height: 80vmin; width: 80vmin"
          spinner-color="rgba(1, 1, 1, 0.5)"
          src="https://lh3.googleusercontent.com/pw/AIL4fc-L2Ws535Y1Ejwkjxjrh7sZ_5Wef3y4dI5DhHuMkZOebNgAHujn3UCHUUqsJckSH36LzyRfikkSb1mJMS7q8jq4UXsQgfu4MrZh6N8F3cFPnNzuT17J=w2400"
        />
        <q-scroll-area class="cardText">
          <div style="padding-left: 2%; padding-right: 2%">
            <text>
              <h3>Technical Skills</h3>
              <h5>Programming Languages</h5>

              + HTML ●●●●● <br />
              + Python ●●●●● <br />
              + JavaScript - .Net ●●●●● <br />
              + C ●●●●○ <br />
              + C++ ●●●●○ <br />
              + CSS ●●●●○<br />
              <h5>Frontend</h5>

              + Vue - Vuetify - Quasar ●●●●● <br />
              + Wordpress - Elementor ●●●●● <br />
              + React ●●●●○<br />
              <h5>Databases</h5>

              + SQL - MySQL ●●●●● <br />
              + MongoDB ●●●●○ <br />
              + Firebase ●●●●○ <br />
              <h5>Engines</h5>
              + Unity ●●●●○<br />
              + Unreal Engine 5 ●●●●○ <br />
              + Godot ●●○○○<br />
              <h5>Tools</h5>

              + Studio Code ●●●●● <br />
              + GitHub ●●●●● <br />
              + Office 365 & Figma ●●●●● <br />
              + Postman ●●●●○<br />
              + SSMS ●●●●○ <br />
              + Docker ●●●●○<br />
            </text>
          </div>
        </q-scroll-area>
      </q-card>
      <q-card id="card_4" class="column card q-ml-xl" flat>
        <q-img
          loading="lazy"
          style="ratio: 1; opacity: 40%; height: 80vmin; width: 80vmin"
          spinner-color="rgba(1, 1, 1, 0.5)"
          src="https://lh3.googleusercontent.com/pw/AIL4fc_ezoU5_WugYaOamdGG4iCfR66wmoK-EDrNJyytxytf88Al8BrWVcLSsqdBuOOJSDPMEA_G_eIDw_EO3Jj-uC5x4XFYd6G18JoGtkwWS1IAox4zMNoY=w2400"
        />
        <q-scroll-area class="cardText">
          <div style="padding-left: 2%; padding-right: 2%">
            <h3>Personality Traits</h3>
            <h4>Soft Skills</h4>
            + Teamwork <br />
            + Active listening <br />
            + Confidence <br />
            + Creativity <br />
            + Patience <br />
            + Attention to detail <br />
            + Assertive communication <br />
            + Adaptability<br />
            + Proactivity<br />
            <h4>Hobbies</h4>
            + Exercise <br />
            + Art <br />
            + Gaming <br />
            + Music <br />
            + Series <br />
            + Hangouts<br />
          </div>
        </q-scroll-area>
      </q-card>
    </div>
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
      scrollShown: false,
      pageState: 0,
      wait: 0,
    };
  },
  created() {
    console.log(this.saheight);
    console.log(this.sawidth);

    this.unwatch = this.$watch("extend", (val) => {
      if (val) {
        const hover = document.getElementById("extend_notification_text");
        hover.classList.add("move_away");
        const scroll = document.getElementById("Scroll");
        scroll.classList.add("visible_scroll");
        this.scrollShown = true;
        this.unwatch();
      }
    });

    setTimeout(() => {
      const scroll = document.getElementById("Scroll");
      scroll.classList.add("visible_scroll");
      this.scrollShown = true;
    }, 2000);

    onwheel = (mouse) => {
      //console.log(mouse.deltaY);
      if (mouse.deltaY > 99 && this.wait - Date.now() <= 0) {
        this.wait = Date.now() + 1000;
        switch (this.pageState) {
          case 0: {
            if (this.scrollShown) {
              this.card_menu();
              this.pageState = 1;
            }
            break;
          }
          case 1: {
            this.slide(1);
            this.pageState = 2;
            break;
          }
          case 2: {
            this.slide(2);
            this.pageState = 3;
            break;
          }
          case 3: {
            this.slide(3);
            this.pageState = 4;
            let element = document.getElementById("Opener");
            element.style.transition = "all 0s";
            element.style.opacity = 0;
            element.classList.remove("show_cards_a");
            element.classList.add("show_cards_b");
            break;
          }
          case 4: {
            this.down_to_main();
            this.pageState = 0;
            break;
          }
        }
      }
      if (mouse.deltaY < -99 && this.wait - Date.now() <= 0) {
        this.wait = Date.now() + 1000;
        switch (this.pageState) {
          case 1: {
            this.leave_card_menu();
            this.pageState = 0;
            break;
          }
          case 2: {
            this.slide(0);
            this.pageState = 1;
            break;
          }
          case 3: {
            this.slide(1);
            this.pageState = 2;
            let element = document.getElementById("Opener");
            element.style.transition = "all 0s";
            element.style.opacity = 0;
            element.classList.add("show_cards_a");
            element.classList.remove("show_cards_b");
            cards.style.removeProperty("opacity");
            break;
          }
          case 4: {
            this.slide(2);
            this.pageState = 3;
            break;
          }
        }
      }
    };
  },
  methods: {
    card_menu() {
      let element = document.getElementById("Opener");
      element.classList.add("show_cards_a");
      element = document.getElementById("Cards");
      element.classList.remove("show_cards_a");
      element.classList.remove("show_cards_b");
    },

    leave_card_menu() {
      let element = document.getElementById("Opener");
      element.classList.remove("show_cards_a");
      let cards = document.getElementById("Cards");
      cards.style.removeProperty("transform");
      cards.classList.add("show_cards_b");
    },

    down_to_main() {
      let element = document.getElementById("Opener");
      element.style.transition = "all 2s";

      let cards = document.getElementById("Cards");
      cards.style.removeProperty("transform");
      element.style.removeProperty("opacity");
      cards.classList.add("show_cards_a");
      element.classList.remove("show_cards_b");
    },

    slide(n) {
      let cards = document.getElementById("Cards");
      cards.style.transform = "translateX(" + -25 * n + "%)";
    },
  },
  components: {
    NameAnim,
    StaryBg,
  },
};
</script>
