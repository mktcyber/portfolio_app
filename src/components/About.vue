<template>
    <article>
    <h2>A little about me</h2>
    <p>
    I am an Inquisitive, experienced full stack developer, with a good foundation in math, logic, and
    cross-platform coding. Enthusiastic Software Engineer/Data Science experience participating in the complete
    product development lifecycle of successfully launched applications. I am proficient in the the following areas
      <span
        ref="reactive"
        @mouseenter="reactiveHighlight"
        @mouseleave="reactiveHighlightRemove"
        >HTML, CSS, JavaScript, PHP and Python</span
      >
      and modern frameworks like
      <span
        ref="gdesign"
        @mouseenter="gHighlight"
        @mouseleave="gHighlightRemove"
        >VueJs and Laravel</span
      >
      . Always puts effort in making User Interface beautiful and practical with
      tools like
      <span
        ref="uidesign"
        @mouseenter="uiHighlight"
        @mouseleave="uiHighlightRemove"
        >Figma.</span>
    </p>
    <p>
      In my free time I work on cool projects in Machine Learning.
    </p>
    <ul>
      <li>
        <img :src="js" alt="javascipt" />
      </li>
      <li>
        <img :src="image1" alt="vuejs" />
      </li>
      <li>
        <img :src="laravel" alt="laravel" />
      </li>
      <li>
        <img :src="java" alt="nodejs" />
      </li>
      <li>
        <img :src="python" alt="photoshop" />
      </li>
      <li>
        <img :src="machine" alt="figma" />
      </li>
      <li>
        <a>
          <button>Resume</button>
        </a>
      </li>
    </ul>
  </article>
</template>
<script>
import { TimelineLite } from "gsap/dist/gsap";
export default {
    name:'AboutPage',

    data(){
       return{
       image1:'/assets/image1.svg',
       laravel:'/assets/laravel.svg',
       js:'/assets/js.gif',
       java:'/assets/java.png',
       python:'/assets/python.png',
       machine:'/assets/machine-learning.png',
       }
   },
    methods: {
    reactiveHighlight() {
      const tl = new TimelineLite();
      const { reactive } = this.$refs;
      tl.to(reactive, {
        backgroundColor: "#1a1a1a",
        color: "white",
      });
    },
    reactiveHighlightRemove() {
      const tl = new TimelineLite();
      const { reactive } = this.$refs;
      tl.to(reactive, {
        backgroundColor: "#141414",
        color: "#8d8d8d",
      });
    },
    uiHighlight() {
      const tl = new TimelineLite();
      const { uidesign } = this.$refs;
      tl.to(uidesign, {
        backgroundColor: "#1a1a1a",
        color: "white",
      });
    },
    uiHighlightRemove() {
      const tl = new TimelineLite();
      const { uidesign } = this.$refs;
      tl.to(uidesign, {
        backgroundColor: "#141414",
        color: "#8d8d8d",
      });
    },
    gHighlight() {
      const tl = new TimelineLite();
      const { gdesign } = this.$refs;
      tl.to(gdesign, {
        backgroundColor: "#1a1a1a",
        color: "white",
      });
    },
    gHighlightRemove() {
      const tl = new TimelineLite();
      const { gdesign } = this.$refs;
      tl.to(gdesign, {
        backgroundColor: "#141414",
        color: "#8d8d8d",
      });
    },
  },
}
</script>
<style scoped>
/* article{
    background-color: #1c1c1c;
    margin-top: 200px;
    margin-bottom: 200px;
} */
p {
  font-size: clamp(16px, 1.2vw, 1.2vw);
  line-height: 2;
  color: #9d9d9d;
  /* margin: 50px; */
  text-align: center;
  
}

h2 {
  font-size: clamp(24px, 3vw, 3vw);
  font-weight: 300;
  margin: 0;
  margin-top: 200px;
  margin-right: 1350px;
}
ul {
  margin-top: clamp(3em, 4vw, 4vw);
  list-style-type: none;
  display: flex;
  justify-content: space-around;
  margin-bottom: 200px;
}
img {
  height: 30px;
  filter: grayscale();
  transition: filter 0.2s ease-in-out;
}
button {
  height: 30px;
  border: none;
  font-size: 18px;
  font-weight: 900;
  background-color: white;
  cursor: pointer;
  transition: background-color 0.2s ease-in-out;
}

button:hover {
  background-color: #59ff9c;
}

img:hover {
  filter: none;
}

span {
  background-color: #141414;
  margin: 0.3em;
  padding: 0.3em 0.7em;
  color: #8d8d8d;
}

@media (max-width: 700px) {
  img,
  button {
    height: 20px;
  }
}
</style>