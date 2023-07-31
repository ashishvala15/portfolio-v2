<template>
  <section class="skills-section" id="skills">
    <SectionHeader :text="'SKILLS'" />
    <div class="skills">
      <div class="skillset--1">
        <h2>
          <span>ANGULAR</span> . <span>REACTJS</span> .
          <span>NODEJS</span> . <span>ANGULAR</span> .
          <span>JAVASCRIPT</span> . <span>REACTJS</span> .
          <span>TYPESCRIPT</span> . <span>NODEJS</span>
        </h2>
      </div>
      <div class="skillset--2">
        <h2>
          <span>NET</span> . <span>MVC</span> . <span>gRPC</span> .
          <span>AWS</span> . <span>NET</span> . <span>C#</span> .
          <span>AWS</span> . <span>GIT</span> . <span>NET</span> .
          <span>C#</span> . <span>AWS</span> . <span>GIT</span>
        </h2>
      </div>
      <div class="skillset--1">
        <h2>
          <span>MSSQL</span> . <span>POSTGRESQL</span> . <span>MYSQL</span> . <span>AZURE</span> .
          <span>AZURE</span> . <span>POSTGRESQL</span> . <span>MYSQL</span> . <span>MONGODB</span> .
          <span>MSSQL</span> . <span>MONGODB</span> . <span>AZURE</span> . <span>POSTGRESQL</span>
        </h2>
      </div>
      <div class="skillset--2">
        <h2>
          <span>HTML</span> . <span>CSS</span> . <span>SCSS</span> .
          <span>Bootstrap</span> . <span>HTML</span> . <span>CSS</span> .
          <span>SCSS</span> . <span>Bootstrap</span>
        </h2>
      </div>
    </div>
  </section>
</template>

<script setup>
import { onMounted } from "vue";
import SectionHeader from "./SectionHeader.vue";
import gsap from "gsap";
import ScrollTrigger from "gsap/ScrollTrigger";
gsap.registerPlugin(ScrollTrigger);

onMounted(() => {
  const tl = gsap.timeline({
    scrollTrigger: {
      trigger: ".skills-section .skills",
      start: "top bottom",
      end: "bottom+=200 top",
      scrub: true,
    },
  });

  tl.fromTo(".skillset--1 h2", { x: "20%" }, { x: "-20%" }, 0).fromTo(
    ".skillset--2 h2",
    { x: "-20%" },
    { x: "20%" },
    0
  );
});
</script>

<style lang="scss" scoped>
@import "@/assets/variables.scss";
</style>
