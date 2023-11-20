<template>
  <v-app id="home">
    <NavBar />
    <v-container fluid class="container">
      <div class="head">
        <v-row>
          <v-col cols="5">
            <div style="position: relative" class="mt-16">
              <h1 class="text-grey">Hello</h1>
              <h1 class="text-white">I'M Alex Ciobanu</h1>
              <span class="text-grey">Front End Developer</span><br />
              <v-btn tile dark class="text-yellow mt-8" variant="outlined">
                Contact me
              </v-btn>
            </div>
          </v-col>
          <v-col cols="2">
            <div style="
                position: absolute;
                z-index: 9999;
                bottom: 0;
                margin-left: auto;
                margin-right: auto;
                left: 0;
                right: 0;
                text-align: center;
                color: white;
              ">
              <v-icon>fas fa-angle-double-down</v-icon>
            </div>
          </v-col>
          <v-col cols="5">
            <div style="position: relative; z-index: 9999" class="mt-16">
              <v-img src="man.png" contain max-height="400"></v-img>
            </div>
          </v-col>
        </v-row>
        <v-row>
          <v-col cols="12" sm="6">
            <div class="egg">
              <v-img src="v1.png" max height="300"></v-img>
            </div>
          </v-col>
          <v-col cols="12" sm="5">
            <h3 class="mt-16">About Me </h3>
            <div style="width: 200px; margin: 0 auto">
              <v-slider v-model="slider2" color="yellow" label=""></v-slider>
            </div>
            <h4 class="mt-4">I am a Creative Web Designer</h4>
            <h4>And Developer</h4>
            <p class="text-grey">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore
              in, sint rerum consectetur neque aliquid optio, fugit itaque
              maiores eos fuga totam atque eius esse voluptates, dignissimos et
              architecto quas!
            </p>
            <p class="text-grey">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Non,
              expedita consectetur porro ex eveniet doloremclue, dolore in quas,
              eum labore laborum a hic pariatur? Consectetur, aspernatur? Ex
              eaque quibusdam iste.
            </p>
            <v-btn tile dark color="yellow" class="mt-15">
              Download Resume
            </v-btn>
          </v-col>
        </v-row>
      </div>
      <div class="text-center mt-9" style="margin-bottom: 50px;">
        <h2>What I Do</h2>
        <div style="width: 200px; margin: 0 auto">
          <v-slider v-model="slider2" color="yellow" label="" style="height: 100px; width: 200px"></v-slider>
        </div>
      </div>
      <v-col cols="12" class="padd" id="portfolio">
        <div class="first" id="project">
       <v-col cols="5">
            <v-row>
              <v-col>
                <div class="child">
                  <v-btn icon="mdi-laptop" color="yellow" class="black"></v-btn>
                  <h3 class="ml-3 mt-4">Web Design</h3>
                  <p class="text-grey ml-3 mt-4 text-caption">
                    Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                    <br />
                    quae ullam, adipisci voluptatum corrupti porro magnam suscipit
                    a aperiam rerum unde <br />error et cupiditate repellendus
                    quaerat ratione soluta eius minima.
                  </p>
                </div>
              </v-col>

              <v-col>
                <div class="child">
                  <v-btn icon color="yellow" class="red">
                    <v-icon> mdi-cellphone </v-icon>
                  </v-btn>

                  <h3 class="ml-3 mt-4">App Design</h3>
                  <p class="text-grey ml-3 mt-4 text-caption">
                    Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                    <br />
                    quae ullam, adipisci voluptatum corrupti porro magnam suscipit
                    a aperiam rerum unde <br />error et cupiditate repellendus
                    quaerat ratione soluta eius minima.
                  </p>
                </div>
              </v-col>

              <v-col>
                <div class="child">
                  <v-btn icon="mdi-camera" color="yellow" class="black"></v-btn>
                  <h3 class="ml-1 mt-1">Photography</h3>
                  <p class="text-grey ml-3 mt-4 text-caption">
                    Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                    <br />
                    quae ullam, adipisci voluptatum corrupti porro magnam suscipit
                    a aperiam rerum unde <br />error et cupiditate repellendus
                    quaerat ratione soluta eius minima.
                  </p>
                </div>
              </v-col>
            </v-row>
          </v-col>
        <v-divider></v-divider>
        </div>
      </v-col>
      <v-col cols="12" sm="12" id="services">
        <div class="d-flex justify-center mb-6">
          <v-btn color="yellow" class="mr-2">All</v-btn>
          <v-btn class="mr-2" variant="tonal">Web Designer</v-btn>
          <v-btn class="mr-2" variant="tonal">Fon Designer</v-btn>
          <v-btn class="mr-2" variant="tonal">Photography</v-btn>
          <v-btn variant="tonal">ILLUSTRATION</v-btn>
        </div>
      </v-col>
      <v-container>
        <v-row>
          <v-col v-for="(item, index) in items" :key="index" cols="12" sm="4">
            <v-card>
              <v-img :src="`/${item.img}`" height="200px" cover></v-img>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
     <v-col cols="12" sm="12">
        <div class="d-flex justify-center mb-6">
          <v-btn color="yellow" class="mt-4">Load More</v-btn>
        </div>
      </v-col>
      <v-col cols="12" id="page">
        <div class="pre">
          <template>
            <v-row>
              <v-col v-for="(card, index) in cards" :key="index" cols="12" sm="4">
                <v-card class="mw-auto" max-width="344" height="1500">
                  <v-img :src="card.img" height="200px" cover></v-img>
                  <v-card-title>{{ card.title }}</v-card-title>
                  <v-card-subtitle>{{ card.subtitle }}</v-card-subtitle>
                  <v-card-text>{{ card.text }}</v-card-text>
                </v-card>
              </v-col>
            </v-row>
          </template>
           <v-row>
           <v-col cols="12" sm="4">
              <v-card class="mw-auto" max-width="344" height="">
                <v-img src="v11.jpg" height="200px" cover></v-img>
                <v-card-title>We provide you the best</v-card-title>
                <v-card-subtitle>
                  By Alex Ciobanu | 15 nov 2023
                </v-card-subtitle>
                <v-card-text>
                  Lorem ipsum dolor, sit amet consectetur adipisicing elit.
                  Dolor, similique?
                </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" sm="4">
              <v-card class="mw-auto" max-width="344" height="">
                <v-img src="v12.jpg" height="200px" cover></v-img>
                <v-card-title>We provide you the best</v-card-title>
                <v-card-subtitle>
                  By Alex Ciobanu | 15 nov 2023
                </v-card-subtitle>
                <v-card-text>
                  Lorem ipsum dolor, sit amet consectetur adipisicing elit.
                  Dolor, similique?
                </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" sm="4">
              <v-card class="mw-auto" max-width="344" height="">
                <v-img src="v13.jpg" height="200px" cover></v-img>
                <v-card-title>We provide you the best</v-card-title>
                <v-card-subtitle>
                  By Alex Ciobanu | 15 nov 2023
                </v-card-subtitle>
                <v-card-text>
                  Lorem ipsum dolor, sit amet consectetur adipisicing elit.
                  Dolor, similique?
                </v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <v-col cols="9" id="blog">
        <div class="hire">
          <v-row>
            <v-col cols="15" sm="8">
              <h1 class="mt-9">Hire me for your awesome project</h1>
              <p class="text-gray">
                Lorem ipsum, dolor sit amet consectetur adipisicing elit. A
                dolorum consequatur magnam. Odit, tempore. Consequatur.
              </p>
            </v-col>

            <v-col cols="12" sm="12">
              <div class="d-flex justify-center mb-6">
                <v-btn color="yellow" class="mt-4">Hire me</v-btn>
              </div>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <v-col cols="12" sm="12" class="px-16" id="contact">
        <v-row>
          <v-col cols="12" sm="4">
            <div class="child">
              <h1>Contact info.</h1>
              <v-btn icon class="mt-10" variant="outlined">
                <v-icon>mdi-map-marker</v-icon>

              </v-btn><br />
              <span class="text-caption">Your Street SYO,Your Area Dream</span><br />
              <v-btn icon="mdi-phone" class="mt-10" variant="outlined"></v-btn><br />
              <span class="text-caption">00215 -6547</span><br />
              <span class="text-caption">00215 -6547</span><br />

              <v-btn icon="mdi-email" class="mt-10" variant="outlined"></v-btn><br />
              <span class="text-caption">adevarul00@inbox.ru</span><br />
              <span class="text-caption">adevarul00@inbox.ru</span><br />
            </div>
          </v-col>
          <v-col cols="12" sm="8">
            <h1 class="mt-8">Send your message</h1>
            <v-divider></v-divider>
            <span class="text-caption">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. Iure,
              corporis nihil. Eveniet atque expedita numquam architecto, quis
              repellendus maiores obcaecati!
            </span>
            <v-row class="mt-15">
              <v-col cols="15" sm="6">
                <v-text-field label="Name" persistent-hint variant="outlined"></v-text-field>
              </v-col>
            </v-row>
            <v-col cols="15" sm="6">
              <v-text-field label="Message" persistent-hint variant="outlined"></v-text-field>
              <v-btn color="yellow" class="mt-8">Submit Now</v-btn>

            </v-col>
          </v-col>
        </v-row>
      </v-col>
    </v-container>
    <FooterView />
  </v-app>
  <div id="app">
    <footer>
      <div class="bg-grey text-center">
        <div style="width: 100%;">
          <div>
            <button class="btn mx-5" style="color: white;">
              <i class="fas fa-university"></i>
            </button>
            <button class="btn mx-5" style="color: yellow;">
              <i class="fas fa-wifi"></i>
            </button>
            <button class="btn mx-5" style="color: white;">
              <i class="fas fa-podcast"></i>
            </button>
            <button class="btn mx-5" style="color: yellow;">
              <i class="fas fa-comment"></i>
            </button>

            <div class="text-black">
              @ {{ new Date().getFullYear() }}
              <strong>Alex Ciobanu All Rights Reserved</strong>
            </div>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>
<script>
import { defineComponent } from "vue";
import NavBar from "@/components/NavBar.vue";

export default defineComponent({
  name: "HomeView",
  setup() {
    return {
      slider2: 50,
      items: [
        {
          img: "v10.jpg",
        },
        {
          img: "v5.jpg",
        },
        {
          img: "v3.png",
        },
        {
          img: "v7.jpg",
        },
        {
          img: "v4.png",
        },
        {
          img: "v8.jpg",
        },
      ],
    };
  },

  components: {
    NavBar,
  },
});
</script>

<style scoped>
.container {
  padding: 16px 0;
}

.head {
  position: relative;
  text-align: center;
  padding: 15px;
  margin-bottom: 5px;
  height: 400px;
  width: 100%;
  color: black
}

.head::before {
  content: " ";
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 50%;
  background: blue;
  transform: skew(0deg, 5deg);
}

.head::after {
  content: " ";
  position: absolute;
  top: 0;
  right: 0;
  height: 100%;
  width: 50%;
  background: blue;
  transform: skew(0deg, -5deg);
}

.egg {
  display: block;
  margin-left: 100px;
  margin-top: 50px;
  width: 356px;
  height: 300px;
  background-color: yellow;
  border-radius: 50% 50% 50% 50%/60% 60% 40% 0%;
}

.first {
  width: 190%;
  height: 188px;
  text-align: center;
  padding: 25rem 25rem;
}

.child {
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: center;
  margin-right: 50px;
}

.imghHover {
  padding: 0 200px;
}

.pre {
  widows: 100%;
  height: 400px;
  text-align: center;
  padding: 200px;
  background-color: blue;
}

.hire {
  width: 134%;
  height: 200px;
  padding: 200px;
  background-color: grey;
  margin-top: -25px;
}
</style>