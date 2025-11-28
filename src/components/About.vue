<script setup>
import {
  ArrowRightIcon,
  ChatBubbleLeftRightIcon,
  CodeBracketSquareIcon,
  CubeIcon,
  PaintBrushIcon,
  ServerIcon,
} from "@heroicons/vue/16/solid";

import about1 from "/src/assets/coding.jpg";
import about2 from "/src/assets/creativity.jpg";
import about3 from "/src/assets/indie.jpg";
import about4 from "/src/assets/happyd.jpg";

const aboutImage = [
  {
    id: 1,
    src: about1,
    alt: "coding",
    gradient: `bg-linear-to-r from-blue-600 to-cyan-600 border-blue-400/40`,
    badge: "Professional",
    badgeColor: "bg-blue-500",
    animation: "fade-right",
    delay: 200,
  },
  {
    id: 2,
    src: about2,
    alt: "yay 222",
    gradient: `bg-linear-to-r from-blue-500 to-cyan-500 border-blue-400/40`,
    badge: "Creative",
    badgeColor: "bg-cyan-500",
    animation: "fade-left",
    delay: 300,
  },
  {
    id: 3,
    src: about3,
    alt: "yay 333",
    gradient: `bg-linear-to-r from-blue-500 to-cyan-500 border-blue-400/40`,
    badge: "Indie Dev",
    badgeColor: "bg-blue-600",
    animation: "fade-right",
    delay: 400,
  },
  {
    id: 4,
    src: about4,
    alt: "yay 444",
    gradient: `bg-linear-to-r from-blue-600 to-cyan-600 border-blue-400/40`,
    badge: "Happy Designer",
    badgeColor: "bg-cyan-600",
    animation: "fade-left",
    delay: 200,
  },
];

const skills = [
  {
    id: 1,
    icon: CodeBracketSquareIcon,
    iconColor: "text-blue-400",
    title: "Frontend",
    desc: "Vue, Javascript, Tailwind CSS",
  },
  {
    id: 2,
    icon: ServerIcon,
    iconColor: "text-cyan-400",
    title: "Backend",
    desc: "Java, Spring, Python, Flask, SQL, REST APIs",
  },
  {
    id: 3,
    icon: PaintBrushIcon,
    iconColor: "text-blue-400",
    title: "Design",
    desc: "Inkscape, Responsive Design, Prototyping",
  },
  {
    id: 4,
    icon: CubeIcon,
    iconColor: "text-cyan-400",
    title: "Tools",
    desc: "Git, Docker, AWS, VSCode",
  },
];

const ctaButtons = [
  {
    id: 1,
    text: "View Portfolio",
    icon: ArrowRightIcon,
    iconclass: `ml-2 group-hover:translate-x-1
        transition-transform`,
    classes: `bg-linear-to-r from-blue-600 to-cyan-600
        text-white hover:from-blue-500 hover:to-cyan-500`,
    url: "#projects"
  },
  {
    id: 2,
    text: "Contact Me",
    icon: ChatBubbleLeftRightIcon,
    iconclass: `mr-2`,
    classes: `border border-blue-400 text-blue-400
        hover:bg-blue-400/10`,
    url: "#contact"
  },
];
</script>

<template>
  <section
    class="relative py-20 overflow-hidden min-h-screen flex items-center"
    id="about"
  >
    <div
      class="w-full px-5 sm:px-8 md:px-12 lg:px-8 max-w-5xl lg:max-w-7xl mx-auto relative z-10"
    >
      <div class="grid lg:grid-cols-2 gap-10 xl:gap-14 items-center">
               <!-- Text -->
        <div class="flex flex-col justify-center order-1 lg:order-2">
          <div class="text-center lg:text-left" data-aos="fade-left">
            <h2
              class="text-white font-bold text-4xl md:text-5xl lg:text-6xl leading-tight"
            >
              About
              <span
                class="text-transparent bg-clip-text bg-linear-to-r from-blue-400 to-cyan-400"
                >Me</span
              >
            </h2>
            <p
              class="text-blue-200 font-medium text-lg md:text-xl mt-4"
              data-aos="fade-left"
              data-aos-delay="100"
            >
              풀스택 프로그래머를 목표로 디자인 공부도 함께 하고 있습니다
            </p>
          </div>
          <p
            class="text-gray-300 pt-4 text-center lg:text-left text-lg leading-relaxed"
            data-aos="fade-left"
            data-aos-delay="200"
          >
            컴퓨터를 매우 좋아하고, 언젠가 모두에게 의미있고 실용적인 서비스를 만드는 것을 목표로
            매일매일 새로운 것을 배워 나가고 있습니다 가상머신과, 컨테이너화 그리고 
            UI/UX 디자인, 잉크스케이프, 반응형 디자인에 관심이 많습니다 최근에는 Vue를 공부하고 있습니다

          </p>
          <div
            class="grid grid-cols-1 sm:grid-cols-2 gap-6 pt-8"
            data-aos="fade-up"
            data-aos-delay="300"
          >
            <div v-for="skill in skills" :key="skill.id" class="flex flex-col">
              <div class="flex items-center gap-3 mb-3">
                <component
                  :is="skill.icon"
                  class="w-6 h-6"
                  :class="skill.iconColor"
                ></component>
                <h3 class="text-lg font-bold text-white">
                  {{ skill.title }}
                </h3>
              </div>
              <p class="text-blue-100 text-sm">
                {{ skill.desc }}
              </p>
            </div>
          </div>
          <div
            class="flex gap-4 pt-8 flex-col sm:flex-row mb-10"
            data-aos="fade-up"
            data-aos-delay="400"
          >

          <div class="flex gap-4 pt-8 flex-col sm:flex-row mb-10"
          data-aos="fade-up"
          data-aos-delay="400"
          >
          <a 
          v-for="button in ctaButtons"
          :key="button.id"
          :href="button.url"
          class="px-8 py-3 rounded-xl font-semibold transition-all duration-300
          flex items-center justify-center"
          :class="button.classes"
          >

          <component
          :is="button.icon"
          class="w-5 h-5"
          :class="button.iconclass"
           />
           {{ button.text }}
          </a>

          </div>
          </div>
        </div>
        <div
          class="lg:h-full flex justify-center lg:justify-start order lg:order-1"
        >
        
          <div class="relative w-full max-w-md">
            <div
              data-aos="zoom-in"
              class="relative bg-linear-to-br from-gray-800/60 to-blue-900/40 rounded-3xl backdrop-blur-sm border border-blue-500/30 shadow-2xl p-6"
            >
              <div class="grid grid-cols-2 gap-4">
                <div
                  v-for="(image, index) in aboutImage"
                  :key="image.id"
                  class="relative group"
                  :data-aos="image.animation"
                  :data-aos-delay="image.delay"
                >
                  <div
                    class="rounded-2xl p-2 border shadow-lg"
                    :class="image.gradient"
                  >
                    <img
                      :src="image.src"
                      :alt="image.alt"
                      class="w-full h-48 object-cover rounded-xl group-hover:scale-105 transition-transform duration-300"
                    />
                  </div>
                  <div
                    class="absolute -top-2 -right-2 text-white text-xs px-2 py-1 rounded-full font-semibold"
                    :class="image.badgeColor"
                  >
                    {{ image.badge }}
                  </div>
                </div>
              </div>
              <div
                class="absolute -bottom-4 left-1/2 transform -translate-x-1/2 z-20 bg-linear-to-r from-blue-500 to-cyan-500 rounded-2xl px-6 py-3 border border-blue-400/40 shadow-xl"
                data-aos="fade-up"
                data-aos-delay="600"
              >
                <div class="text-center text-white text-xl font-bold">
                  2+ Years Experience
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped></style>
