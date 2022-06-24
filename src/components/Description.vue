<template>
  <article>
    <h2 class="text-white">A little about me</h2>
    <p>
      Inquisitive, energetic computer science specialist skilled in leadership, with a good foundation in math, logic, and
      cross-platform coding. I am a Full-stack Developer experienced in building responsive web apps
      while keeping the aesthetic integrity. Experienced participating in the complete
      product development lifecycle of successfully launched applications. Seeking to leverage solid skills in
      collaboration, communication, and development as a programmer/researcher to contribute to the development
      of technology in my region
      . Proficient in semantic
      <span
        ref="reactive"
        @mouseenter="reactiveHighlight"
        @mouseleave="reactiveHighlightRemove"
        >HTML, CSS, JavaScript</span
      >
      and modern frameworks like
      <span
        ref="gdesign"
        @mouseenter="gHighlight"
        @mouseleave="gHighlightRemove"
        >Laravel and Vuejs</span
      >
      . Always puts effort in making User Interface beautiful and practical with
      tools like
      <span
        ref="uidesign"
        @mouseenter="uiHighlight"
        @mouseleave="uiHighlightRemove"
        >Figma</span
      >
      .
    </p>
    <p>
      In my free time I work on cool projects while experimenting with new
      technologies especially in the field of AI. Currently I'm working on OCR a document, form, or invoice with Tesseract, OpenCV, and Python.
    </p>
    <ul>
      <li>
        <img src="../assets/icons/js.gif" alt="javascipt" />
      </li>
      <li>
        <img src="../assets/icons/vue.svg" alt="vuejs" />
      </li>
      <li>
        <img src="../assets/icons/laravel.svg" alt="Laravel" />
      </li>
      <li>
        <img src="../assets/icons/java.png" alt="Java" />
      </li>
      <li>
        <img src="../assets/icons/python.png" alt="python" />
      </li>
      <li>
        <img src="../assets/icons/figma.svg" alt="figma" />
      </li>
      <li>
        <img src="../assets/icons/machine-learning.png" alt="figma" />
      </li>
      <li>
        <a :href="pdf" download>
          <button>Resume</button>
        </a>
      </li>
    </ul>
  </article>
</template>

<script>
import { TimelineLite } from "gsap/dist/gsap";
export default {
  name: "DescriptionComponent",
  data() {
    return {
      pdf: "../assets/cv.pdf"
    };
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
};
</script>

<style scoped>

p {
  font-size: clamp(16px, 1.2vw, 1.2vw);
  line-height: 2;
  color: #9d9d9d;
}

h2 {
  font-size: clamp(24px, 3vw, 3vw);
  font-weight: 300;
  margin: 0;
}
ul {
  margin-top: clamp(3em, 4vw, 4vw);
  list-style-type: none;
  display: flex;
  justify-content: space-around;
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