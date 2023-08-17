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
            @click="page_state('+')"
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
    <div id="Cards" class="cards show_cards_b">
      <div id="Cards_sub" data-dragstart="0" moveX="0" class="row no-wrap justify-between" >
        <q-card @click="page_state(1)" id="card_1" class="column card card_blur" flat>
          <q-img
            loading="lazy"
            style="ratio: 1; opacity: 60%; height: 80vmin; width: 80vmin"
            spinner-color="rgba(1, 1, 1, 0.5)"
            src="https://lh3.googleusercontent.com/pw/AIL4fc8Nb2Bhg-eiIk4ZmweNPjSdaGAomwVS5WPgeS4JR1ZhfJZISRVTo_IiOxJkcaeC3MweE6JUz8iu9EqGixI8tSEOQfbinW310ScTXg3zcRhLovPjIsY0=w2400"
          />
          <q-scroll-area @scroll="stopscroll = Date.now() + 300" id="scroll_area_1" class="cardText">
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
        <q-card @click="page_state(2)" id="card_2" class="column card card_blur" flat>
          <q-img
            loading="lazy"
            style="ratio: 1; opacity: 60%; height: 80vmin; width: 80vmin"
            spinner-color="rgba(1, 1, 1, 0.5)"
            src="https://lh3.googleusercontent.com/pw/AIL4fc-RUC6_8H2n1pdL_G14lnqRmTY7jpPCjnwZUUCwBhEwhKzE6SKOUD2ToPC9i-xVmYtZt-NAalHK_OaryXzPy6xR6fY-F8MjFfIT5CZ9Bacm3_39Fbqv=w2400"
          />
          <q-scroll-area @scroll="stopscroll = Date.now() + 300" id="scroll_area_2" class="cardText">
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
        <q-card @click="page_state(3)" id="card_3" class="column card card_blur" flat>
          <q-img
            loading="lazy"
            style="ratio: 1; opacity: 60%; height: 80vmin; width: 80vmin"
            spinner-color="rgba(1, 1, 1, 0.5)"
            src="https://lh3.googleusercontent.com/pw/AIL4fc-L2Ws535Y1Ejwkjxjrh7sZ_5Wef3y4dI5DhHuMkZOebNgAHujn3UCHUUqsJckSH36LzyRfikkSb1mJMS7q8jq4UXsQgfu4MrZh6N8F3cFPnNzuT17J=w2400"
          />
          <q-scroll-area @scroll="stopscroll = Date.now() + 300" id="scroll_area_3" class="cardText">
            <div style="padding-left: 2%; padding-right: 2%">
              <text>
                <h3>Technical Skills</h3>
                <h5>Programming Languages</h5>
                <b>+</b> HTML ●●●●● <br />
                <b>+</b> Python ●●●●● <br />
                <b>+</b> JavaScript - .Net ●●●●● <br />
                <b>+</b> C ●●●●○ <br />
                <b>+</b> C++ ●●●●○ <br />
                <b>+</b> CSS ●●●●○<br />
                <br />
                <h5>Frontend</h5>
                <b>+</b> Vue - Vuetify - Quasar ●●●●● <br />
                <b>+</b> Wordpress - Elementor ●●●●● <br />
                <b>+</b> React ●●●●○<br />
                <br />
                <h5>Databases</h5>
                <b>+</b> SQL - MySQL ●●●●● <br />
                <b>+</b> MongoDB ●●●●○ <br />
                <b>+</b> Firebase ●●●●○ <br />
                <br />
                <h5>Game Dev Engines</h5>
                <b>+</b> Unity ●●●●○<br />
                <b>+</b> Unreal Engine 5 ●●●●○ <br />
                <b>+</b> Godot ●●○○○<br />
                <br />
                <h5>Other Tools</h5>
                <b>+</b> Studio Code ●●●●● <br />
                <b>+</b> GitHub ●●●●● <br />
                <b>+</b> Office 365 & Figma ●●●●● <br />
                <b>+</b> Postman ●●●●○<br />
                <b>+</b> SSMS ●●●●○ <br />
                <b>+</b> Docker ●●●●○<br />
                <br />
              </text>
            </div>
          </q-scroll-area>
        </q-card>
        <q-card @click="page_state(4)" id="card_4" class="column card card_blur" flat>
          <q-img
            loading="lazy"
            style="ratio: 1; opacity: 60%; height: 80vmin; width: 80vmin"
            spinner-color="rgba(1, 1, 1, 0.5)"
            src="https://lh3.googleusercontent.com/pw/AIL4fc_ezoU5_WugYaOamdGG4iCfR66wmoK-EDrNJyytxytf88Al8BrWVcLSsqdBuOOJSDPMEA_G_eIDw_EO3Jj-uC5x4XFYd6G18JoGtkwWS1IAox4zMNoY=w2400"
          />
          <q-scroll-area @scroll="stopscroll = Date.now() + 300" id="scroll_area_4" class="cardText">
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
              <br />
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

    <div id="Card_balls" class="show_cards_b cardballs" />
    <div
      @click="balls($event)"
      id="Card_balls_mark"
      style="
        background-image: radial-gradient(rgba(255, 255, 255, 0.5) 45%, transparent 50%);
        background-repeat: no-repeat;
      "
      class="show_cards_b cardballs"
    />

    <div id="JP" class="show_cards_b" style="position: absolute; right: 1em; bottom: 1em; transition: all 3s ease-in-out">
      <q-btn @mouseover="JPwait = Date.now() + 1500" id="mini_button3" push round style="opacity: 1; position: absolute; right: 1.5em; bottom: 1.3em; transition: all 0.5s ease; background-color: rgb(132, 74, 158)" size="3vmin" href="https://github.com/Akisama213/jpmcv" target="_blank">
        <q-img src="/icons8-github.svg" style="height: 6.2vmin; width: 6.2vmin;"/>
      </q-btn>
      <q-btn @mouseover="JPwait = Date.now() + 1500" id="mini_button2" push round style="opacity: 1; position: absolute; right: 1.5em; bottom: 1.3em; transition: all 0.5s ease; background-color: rgb(172, 77, 77)" size="3vmin" href="https://mail.google.com/mail/?view=cm&source=mailto&to=jason1234pm@gmail.com" target="_blank">
        <q-img src="/icons8-gmail.svg" style="height: 5.5vmin; width: 5.5vmin;"/>
      </q-btn>
      <q-btn @mouseover="JPwait = Date.now() + 1500" id="mini_button1" push round style="opacity: 1; position: absolute; right: 1.5em; bottom: 1.3em; transition: all 0.5s ease; background-color: rgb(82, 123, 189)" size="3vmin" href="https://www.linkedin.com/in/jpm213/" target="_blank">
        <q-img src="/icons8-linkedin.svg" style="height: 6vmin; width: 6vmin;"/>
      </q-btn>
      <q-btn @mouseover="JPwait = Date.now() + 1500" push round style="opacity: 1; position: absolute; right: 1em; bottom: 1em; transition: all 1.6s ease; background-color: rgba(180, 180, 180, 1)" size="3.5vmin">
        <q-img id="JP_logo" src="/JP.svg" style="transition: all 0.6s;height: 6vmin; width: 6vmin;" @click="extendJP()"/>
      </q-btn>
    </div>
    </q-page>
</template>
<script>
import NameAnim from "../components/NameAnim.vue";
import StaryBg from "../components/StaryBg.vue";
const scroll = document.getElementById("Scroll");
export default {
  name: "IndexPage",
  data() {
    return {
      extend: false,
      scrollShown: false,
      cardScroll: false,
      stopscroll: false,
      JPwait: 0,
      pageState: 0,
      wait: 0,
    };
  },
  created() {
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
      scroll.classList.add("visible_scroll");
      this.scrollShown = true;
    }, 2000);

    onmousedown = (mouse) => {
      if(this.pageState != 0) {
        let cards_sub = document.getElementById("Cards_sub");
        cards_sub.dataset.dragstart = mouse.clientX;
      }
    }

    onmouseup = ()  => {
      let cards_sub = document.getElementById("Cards_sub");
      cards_sub.dataset.dragstart = "0";
      cards_sub.animate({transform: "translateX(0%)"}, {duration: 1200, fill:"forwards", effect:"ease-out"})
      if(cards_sub.dataset.moveX < -15) {
        this.page_state("+");
      } else if(cards_sub.dataset.moveX > 15) {
        this.page_state("-");
      }
    };

    onmousemove = (mouse) => {
      setTimeout(() =>{
        if(this.JPwait - Date.now() <= 0) {
          this.dextendJP();
        }
      }, 100);
      let cards_sub = document.getElementById("Cards_sub");
      if(cards_sub.dataset.dragstart != 0) {
        const moveX = -50 * Math.min((cards_sub.dataset.dragstart - mouse.clientX) / window.innerWidth);
        cards_sub.dataset.moveX = moveX;
        cards_sub.animate({transform: "translateX(" + moveX + "%)"}, {duration: 1500, fill:"forwards"})
      }
    };

    onwheel = (mouse) => {
      setTimeout(() =>{
        if(this.stopscroll - Date.now() <= 0){
          if (mouse.deltaY > 99) {
            this.page_state("+");
          }
          if (mouse.deltaY < -99) {
            this.page_state("-");
          }
        }
      }, 50);
    };

  },
  methods: {
    page_state(n) {
      if (this.wait - Date.now() <= 0) {
        switch(n){
          case "+" : {
            if(this.pageState < 4) {
              this.wait = Date.now() + 1000;
              if (this.pageState == 0) {
                this.card_menu();
              }
              this.pageState += 1;
              this.slide();
              this.blur();
              this.deblur();
            }
            break
          }
          case "-" : {
            if(this.pageState > 0) {
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
            break
          }
          case 1 : {
            this.pageState = 1;
            this.slide();
            this.blur();
            this.deblur();
            break
          }
          case 2 : {
            this.pageState = 2;
            this.slide();
            this.blur();
            this.deblur();
            break
          }
          case 3 : {
            this.pageState = 3;
            this.slide();
            this.blur();
            this.deblur();
            break
          }
          case 4 : {
            this.pageState = 4;
            this.slide();
            this.blur();
            this.deblur();
            break
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
      let cardsBalls = document.getElementById("Card_balls");
      let cardsBallsM = document.getElementById("Card_balls_mark");
      cardsBalls.classList.remove("show_cards_b");
      cardsBallsM.classList.remove("show_cards_b");
      let JP = document.getElementById("JP");
      JP.classList.remove("show_cards_b");
    },
    leave_card_menu() {
      let element = document.getElementById("Opener");
      element.classList.remove("show_cards_a");
      let cards = document.getElementById("Cards");
      cards.style.removeProperty("transform");
      cards.classList.add("show_cards_b");
      let cardsBalls = document.getElementById("Card_balls");
      let cardsBallsM = document.getElementById("Card_balls_mark");
      cardsBalls.style.removeProperty("transform");
      cardsBalls.classList.add("show_cards_b");
      cardsBallsM.style.removeProperty("transform");
      cardsBallsM.classList.add("show_cards_b");
    },
    slide() {
      let cards = document.getElementById("Cards");
      cards.style.transform = "translateX(" + -25 * (this.pageState - 1) + "%)";
      let cardsBalls = document.getElementById("Card_balls");
      let cardsBallsM = document.getElementById("Card_balls_mark");
      cardsBalls.style.backgroundPosition = ((this.pageState - 1) * 33.3) + "% 0"
      cardsBallsM.style.backgroundPosition = ((this.pageState - 1) * 33.3) + "% 0"
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
    balls(event) {
      if(event.layerX < -40) {
        this.page_state(1);
      } else if(event.layerX < 0) {
        this.page_state(2);
      } else if (event.layerX < 40) {
        this.page_state(3);
      } else {
        this.page_state(4);
      }
    },
    extendJP() {
      let direction;
      this.JPwait = Date.now() + 1500;
      let logo = document.getElementById("JP_logo");
      logo.style.transform = "rotate(180deg)";
      if(window.innerWidth > window.innerHeight)  {
        direction = "X";
      } else {
        direction = "Y";
      }
      for(let n = 1; n<4; n++) {
        let button = document.getElementById("mini_button" + n);
        button.style.transform = "translate" + direction + "(" + (-130*n) +"%)";
      }
    },
    dextendJP() {
      let logo = document.getElementById("JP_logo");
      logo.style.removeProperty("transform");
      for(let n = 1; n<4; n++) {
        let button = document.getElementById("mini_button" + n);
        button.style.removeProperty("transform");
      }
    },
  },
  components: {
    NameAnim,
    StaryBg,
  },
};
</script>
