<template>
  <div class="flex flex-col gap-[2.5rem]">
    <!-- introduction section -->
    <div class="divCenter">
      <p
        id="landing_intro"
        ref="landingIntro"
        class="lg:text-xl text-md acrlyic w-auto text-center selector"
      ></p>
    </div>
    <div class="flex flex-col lg:flex-row">
      <!-- Column 1 -->
      <div class="lg:w-1/2 p-4 order-2 lg:order-1">
        <section>
          <h1 class="text-4xl font-bold">gnf dedsec</h1>
          <h3 class="text-lg">Professional Front-end developer</h3>
          <h3 class="text-lg">B.sc KKU TH</h3>
        </section>
      </div>

      <!-- Column 2 -->
      <div
        class="lg:w-1/2 p-4 order-1 lg:order-2 flex justify-center items-center"
      >
        <section>
          <div
            class="rounded-full overflow-hidden h-48 w-48 border border-white-800 image-container"
          >
            <img
              src="/assets/images/gnf.webp"
              alt="Image description"
              class="w-full h-full object-cover"
            />
          </div>
        </section>
      </div>
    </div>

    <section class="pt-2">
      <h2
        class="lg:text-2xl text-lg font-bold underline underline-offset-8 decoration-2"
      >
        Professional background
      </h2>
      <br />
      <p class="lg:text-lg text-sm text-justify leading-6">
        &nbsp;&nbsp;&nbsp;&nbsp; Professional junior web developer capable
        professional looking and user-friendly websites from stratch and writes
        <strong>performance optimized, reusable and refactorable codes</strong>.
        Professionally developed 5 web applications with multiple Javascript
        frameworks.
      </p>
      <br />
      <p class="lg:text-lg text-sm text-justify leading-6">
        <!-- &nbsp;&nbsp;&nbsp;&nbsp; -->
        Hungry for knowledge, collaborative individual and possess analytical
        skills. Enjoys problem solving and willing to adapt to changes in the
        industry to stay on top.
      </p>
    </section>
    <!-- info section -->
    <section class="">
      <h2
        class="lg:text-2xl text-lg font-bold underline underline-offset-8 decoration-2"
      >
        Bio
      </h2>
      <br />
      <p class="lg:text-lg text-sm text-justify leading-6">
        &nbsp;&nbsp;&nbsp;&nbsp; gnf has a strong passion on technology and
        computers. Outside of programmimg, gnf has a hobby of collecting and
        engage with technology. He likes to tinker with his Arch Linux Operating
        System and enjoys collecting custom keyboards.
      </p>
    </section>
    <!-- journey section -->
    <section class="">
      <h2
        class="lg:text-2xl text-lg font-bold underline underline-offset-8 decoration-2"
      >
        Journey
      </h2>
      <br />
      <div class="flex flex-col gap-2">
        <!-- year 2017 -->
        <p class="lg:text-lg text-sm text-justify">
          <strong>2017:</strong>
          &nbsp; Started journey on programming as a hobby
        </p>
        <!-- year 2020 -->
        <p class="lg:text-lg text-sm text-justify">
          <strong>2020:</strong>
          &nbsp; Enrolled for diploma of ICT with specalism in software
          engineering
        </p>
        <!-- year 2022  -->
        <p class="lg:text-lg text-sm text-justify">
          <strong>2022:</strong>
          &nbsp; Started journey on web development
        </p>
      </div>
    </section>
  </div>
</template>

<script>
import TypeIt from 'typeit';
import 'animate.css';
import { ref } from 'vue';

export default {
	data() {
		return {
			display: false
		};
	},
	setup() {
		const landingIntro = ref('');

		if (landingIntro.value !== '') {
			landingIntro.value === '';
		}
	},
	mounted() {
		new TypeIt('#landing_intro', {
			speed: 50,
			waitUntilVisible: true,
			startDelay: 2000,
			startDelete: true,
			// remove cursor when finished
			afterComplete: function (instance) {
				instance.destroy();
			}
		})
			.type(
				'Hello! I &nbsp; am a frontend  &nbsp; developer &nbsp; based &nbsp; in  &nbsp;Thailand.'
			)
			.go();
	}
};
</script>

<style>
  .lg\:w-1\/2 {
    padding: 0px !important;
  }
  .selector {
    background-color: var(--bg-sel);
  }

  .copyright {
    animation: fadeInLeft; /* referring directly to the animation's @keyframe declaration */
    animation-duration: 1s; /* don't forget to set a duration! */
    animation-delay: 3s;
  }

  /* @keyframes copyright {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
    visibility: visible;
  }
} add*/
  .image-container {
    display: inline-block;
    position: relative;
    width: 200px;
    height: 200px;
  }

  .image-container::before {
    content: '';
    display: block;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border: 3px solid #fff;
    border-radius: 50%;
    opacity: 0;
    animation: pulse 2s infinite;
  }

  @keyframes pulse {
    0% {
      opacity: 0;
      transform: scale(0.9);
    }
    50% {
      opacity: 1;
      transform: scale(1);
    }
    100% {
      opacity: 0;
      transform: scale(0.9);
    }
  }
</style>
