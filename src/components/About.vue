<template>
  <section class="about-section">
    <SectionHeader :text="'ABOUT'" />
    <div class="container">
      <div class="image">
        <div class="image-border"></div>
        <img class="light" alt="Man Looking Up" src="/images/person3.png" />
        <img class="dark" alt="Man Looking Up" src="/images/person.png" />
      </div>

      <div class="text">
        <p>
          <b>Software Engineer</b> with 6+ years of experience in web-based applications, utilizing front-end technologies
          and Microsoft .NET frameworks. Proficient in ASP.NET, MVC, Angular, Node.js, React.js, JavaScript, TypeScript,
          C#, HTML, CSS, .NET, jQuery, MS SQL Server, and PostgreSQL. Strong understanding of technology with a focus on
          delivering business solutions through all phases of the Software Development Life Cycle. Excellent analytical,
          communication, and problem-solving skills, with a proven ability to provide quick fixes and innovative solutions
          to critical problems. Experienced in client interaction and query resolution. A team player with a positive
          attitude, strong communication skills, and the ability to adapt to new technologies and mentor team members.
        </p>

        <button @click.prevent="lenis.scrollTo('#contact')" type="button" class="btn btn_about">
          <span>GET IN TOUCH</span>
        </button>
      </div>
    </div>
  </section>
</template>

<script setup>
import SectionHeader from "./SectionHeader.vue";
import { lenis } from "../helpers/animations";
import gsap from "gsap";
import ScrollTrigger from "gsap/ScrollTrigger";
import { onMounted } from "vue";

gsap.registerPlugin(ScrollTrigger);

onMounted(() => {
  // // const tl = gsap.timeline({});
  // gsap.from(".about-section .image img", {
  //   y: "50%",
  //   opacity: 0,
  //   duration: 0.5,
  //   ease: "Power3.easeOut",
  //   scrollTrigger: {
  //     trigger: ".about-section .container",
  //     start: "top+=500 bottom",
  //     markers: true,
  //   },
  // });
  // gsap.from(".about-section .text", {
  //   y: "50%",
  //   opacity: 0,
  //   scrollTrigger: {
  //     trigger: ".about-section .container",
  //     start: "top+=500 bottom",
  //     markers: true,
  //   },
  // });
});
</script>

<style lang="scss" scoped></style>
