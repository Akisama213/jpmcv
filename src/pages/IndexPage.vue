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
                    opacity: 60%;
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

    <div id="Cards" class="cards show_cards_b" >
      <div id="Cards_sub" class="row no-wrap justify-between" @mousedown="drag($event)">
      <q-card id="card_1" class="column card card_blur" flat>
        <q-img
          loading="lazy"
          style="ratio: 1; opacity: 60%; height: 80vmin; width: 80vmin"
          spinner-color="rgba(1, 1, 1, 0.5)"
          src="https://lh3.googleusercontent.com/pw/AIL4fc8Nb2Bhg-eiIk4ZmweNPjSdaGAomwVS5WPgeS4JR1ZhfJZISRVTo_IiOxJkcaeC3MweE6JUz8iu9EqGixI8tSEOQfbinW310ScTXg3zcRhLovPjIsY0=w2400"
        />
        <q-scroll-area @mouseover="stopscroll = true" @mouseleave="stopscroll = false" id="scroll_area_1" class="cardText">
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
      <q-card id="card_2" class="column card card_blur" flat>
        <q-img
          loading="lazy"
          style="ratio: 1; opacity: 60%; height: 80vmin; width: 80vmin"
          spinner-color="rgba(1, 1, 1, 0.5)"
          src="https://lh3.googleusercontent.com/pw/AIL4fc-RUC6_8H2n1pdL_G14lnqRmTY7jpPCjnwZUUCwBhEwhKzE6SKOUD2ToPC9i-xVmYtZt-NAalHK_OaryXzPy6xR6fY-F8MjFfIT5CZ9Bacm3_39Fbqv=w2400"
        />
        <q-scroll-area @mouseover="stopscroll = true" @mouseleave="stopscroll = false" id="scroll_area_2" class="cardText">
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
      <q-card id="card_3" class="column card card_blur" flat>
        <q-img
          loading="lazy"
          style="ratio: 1; opacity: 60%; height: 80vmin; width: 80vmin"
          spinner-color="rgba(1, 1, 1, 0.5)"
          src="https://lh3.googleusercontent.com/pw/AIL4fc-L2Ws535Y1Ejwkjxjrh7sZ_5Wef3y4dI5DhHuMkZOebNgAHujn3UCHUUqsJckSH36LzyRfikkSb1mJMS7q8jq4UXsQgfu4MrZh6N8F3cFPnNzuT17J=w2400"
        />
        <q-scroll-area @mouseover="stopscroll = true" @mouseleave="stopscroll = false" id="scroll_area_3" class="cardText">
          <div style="padding-left: 2%; padding-right: 2%">
            <text>
              <h3>Technical Skills</h3>
              <div class="justify-between">
                <div class="col">
                  <h5>Programming Languages</h5>

                  <b>+</b> HTML ●●●●● <br />
                  <b>+</b> Python ●●●●● <br />
                  <b>+</b> JavaScript - .Net ●●●●● <br />
                  <b>+</b> C ●●●●○ <br />
                  <b>+</b> C++ ●●●●○ <br />
                  <b>+</b> CSS ●●●●○<br />
                  <br />
                </div>
                <div class="col">
                  <h5>Frontend</h5>

                  <b>+</b> Vue - Vuetify - Quasar ●●●●● <br />
                  <b>+</b> Wordpress - Elementor ●●●●● <br />
                  <b>+</b> React ●●●●○<br />
                  <br />
                </div>
                <div class="col">
                  <h5>Databases</h5>

                  <b>+</b> SQL - MySQL ●●●●● <br />
                  <b>+</b> MongoDB ●●●●○ <br />
                  <b>+</b> Firebase ●●●●○ <br />
                  <br />
                </div>
                <div class="col">
                  <h5>Engines</h5>
                  <b>+</b> Unity ●●●●○<br />
                  <b>+</b> Unreal Engine 5 ●●●●○ <br />
                  <b>+</b> Godot ●●○○○<br />
                  <br />
                </div>
                <div class="col">
                  <h5>Tools</h5>

                  <b>+</b> Studio Code ●●●●● <br />
                  <b>+</b> GitHub ●●●●● <br />
                  <b>+</b> Office 365 & Figma ●●●●● <br />
                  <b>+</b> Postman ●●●●○<br />
                  <b>+</b> SSMS ●●●●○ <br />
                  <b>+</b> Docker ●●●●○<br />
                  <br />
                </div>
              </div>
            </text>
          </div>
        </q-scroll-area>
      </q-card>
      <q-card id="card_4" class="column card card_blur" flat>
        <q-img
          loading="lazy"
          style="ratio: 1; opacity: 60%; height: 80vmin; width: 80vmin"
          spinner-color="rgba(1, 1, 1, 0.5)"
          src="https://lh3.googleusercontent.com/pw/AIL4fc_ezoU5_WugYaOamdGG4iCfR66wmoK-EDrNJyytxytf88Al8BrWVcLSsqdBuOOJSDPMEA_G_eIDw_EO3Jj-uC5x4XFYd6G18JoGtkwWS1IAox4zMNoY=w2400"
        />
        <q-scroll-area @mouseover="stopscroll = true" @mouseleave="stopscroll = false" id="scroll_area_4" class="cardText">
          <div style="padding-left: 2%; padding-right: 2%">
            <h3>Personality Traits</h3>
            <h4>Soft Skills</h4>
            <b>+</b> Teamwork <br />
            <b>+</b> Active listening <br />
            <b>+</b> Confidence <br />
            <b>+</b> Creativity <br />
            <b>+</b> Patience <br />
            <b>+</b> Attention to detail <br />
            <b>+</b> Assertive communication <br />
            <b>+</b> Adaptability<br />
            <b>+</b> Proactivity<br />
            <h4>Hobbies</h4>
            <b>+</b> Exercise <br />
            <b>+</b> Art <br />
            <b>+</b> Gaming <br />
            <b>+</b> Music <br />
            <b>+</b> Series <br />
            <b>+</b> Hangouts<br />
          </div>
        </q-scroll-area>
      </q-card>
    </div>
    </div>
  </q-page>
</template>
<style>

</style>
<script>
import NameAnim from "../components/NameAnim.vue";
import StaryBg from "../components/StaryBg.vue";

export default {
  name: "IndexPage",
  data() {
    return {
      extend: false,
      scrollShown: false,
      cardScroll: false,
      dragging: false,
      stopscroll: false,
      curentX: 0,
      firstX: 0,
      pageState: 0,
      wait: 0,
    };
  },
  watch: {
    currentX(val) {

    }
  },
  created() {
    //let cards = document.getElementById("Cards_sub");

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

    onmousemove = (mouse) => {
      this.currentX = mouse.clientX;
    }

    onwheel = (mouse) => {
      if(!this.stopscroll){
        if (mouse.deltaY > 99) {
          this.page_state("+");
        }
        if (mouse.deltaY < -99) {
          this.page_state("-");
        }
      }
    };
  },
  methods: {
    page_state(n) {
      if (this.wait - Date.now() <= 0) {
        if (n == "+" && this.pageState < 4) {
          this.wait = Date.now() + 1000;
          if (this.pageState == 0) {
            this.card_menu();
          }
          this.pageState += 1;
          this.slide();
          this.blur();
          this.deblur();
        }
        if (n == "-" && this.pageState > 0) {
          this.wait = Date.now() + 1000;
          if (this.pageState == 1) {
            this.pageState -= 1;
            this.leave_card_menu();
          } else {
            this.pageState -= 1;
            this.slide();
            this.blur();
            this.deblur();
          }
        }
      }
    },
    card_menu() {
      let element = document.getElementById("Opener");
      element.classList.add("show_cards_a");
      let cards = document.getElementById("Cards");
      cards.classList.remove("show_cards_a");
      cards.classList.remove("show_cards_b");
    },
    leave_card_menu() {
      let element = document.getElementById("Opener");
      element.classList.remove("show_cards_a");
      let cards = document.getElementById("Cards");
      cards.style.removeProperty("transform");
      cards.classList.add("show_cards_b");
    },
    slide() {
      let cards = document.getElementById("Cards");
      cards.style.transform = "translateX(" + -25 * (this.pageState - 1) + "%)";
    },
    blur() {
      if (this.pageState - 1 > 0) {
        let card = document.getElementById("card_" + (this.pageState - 1));
        card.classList.add("card_blur");
        card.style.transformOrigin = "90% 60%";
      }
      if (this.pageState + 1 < 5) {
        let card = document.getElementById("card_" + (this.pageState + 1));
        card.classList.add("card_blur");
        card.style.transformOrigin = "10% 60%";
      }
    },
    deblur() {
      let card = document.getElementById("card_" + this.pageState);
      card.classList.remove("card_blur");
      card.removeAttribute("transform");
      card.removeAttribute("transform-origin");
    },
    drag(event) {
      this.firstX = event.clientX;
      this.dragging = true;
    },
    scrollingCard(event) {
      this.stopscroll = Date.now() + 2000;
    }
  },
  components: {
    NameAnim,
    StaryBg,
  },
};
</script>
