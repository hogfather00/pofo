<script setup>
import { ArrowDownTrayIcon, ArrowRightIcon } from '@heroicons/vue/16/solid';

</script>

<template>
    <section class="relative w-full overflow-hidden min-h-screen flex items-center">
        <div class="w-full px-5 sm:px-8 md:px-12 lg:px-8 max-w-5xl
        lg:max-w-7xl mx-auto relative z-10
        ">
        <div class="grid lg:grid-cols-2 gap-10 xl:gap-14 items-center">
            <div class="text-white lg:text-left"
                 data-aos="fade-right">
                <h1 class="text-white font-bold text-4xl
                md:text-5xl lg:text-6xl leading-tight">
                반갑습니다 <span
                class="text-transparent bg-clip-text bg-linear-to-r 
                from-blue-400 to-cyan-400"> Min</span>입니다 
                </h1>
                <p class="text-blue-200 font-medium text-lg md:text-xl mt-4"
                data-aos="fade-right"
                data-aos-delay="100"
                >
                    웹개발과 웹디자인 그리고 UI/UX를 공부하고 있습니다
                    </p>
                <p class="text-blue-200 font-medium text-lg md:text-xl mt-4"
                data-aos="fade-right"
                data-aos-delay="500"
                >
                    Web Dev & Design & UI/UX Enthusiast
                </p>
            </div>
            <p class="text-gray-300 pt-6 text-center lg:text-left
            mx-auto max-w-xl text-lg leading-relaxed">
                오랫동안 저의 일을 좋아하며, 의미있는 것들을 만들어 보려고 매일 공부중입니다
                <br />
                Java Spring Vue Javascript TailwindCss Python
                을 사용하고 있습니다
            </p>
            <div class="flex items-center gap-4 pt-8 flex-col
            sm:flex-row sm:w-max sm:mx-auto lg:mx-0"
            data-aos="fade-up"
            data-aos-delay="300"
            >

            <a href="#contact" class="flex items-center justify-center">
            <button
            class="px-8 md:px-10 py-4 rounded-xl relative group
            w-full sm:w-max flex justify-center overflow-hidden
            bg-linear-to-r from-blue-600 to-cyan-600
            hover:from-blue-500 hover:to-cyan-500 transition-all
            duration-300
            "
            >
            <span class="relative flex items-center justify-center
            text-white font-semibold text-lg
            ">연락하기 
            <ArrowRightIcon class="ml-2 w-5 h-5
            group-hover:translate-x-1 transition-transform
            " />
            </span>
        </button>
    </a>
        <a
        href="/Min_(CV).pdf"
        download="이력서_Min.pdf"
        class="px-8 md:px-10 py-4 rounded-xl relative group
        w-auto flex justify-center items-center border-2 border-blue-400
        hover:bg-blue-400/10 transition-all duration-300
        "
        >
        <div class="flex items-center justify-center relative">
            <ArrowDownTrayIcon 
            class="w-5 h-5 text-blue-400 group-hover:translate-y-1 transition-transform"
            />
            <span class="pl-3 text-blue-400 font-semibold text-lg">
                이력서 다운로드
            </span>
        </div>
    </a>
            </div>
            <div class="flex items-center justify-center
            lg:justify-start gap-8 pt-12"
            data-aos="fade-up" data-aos-delay="400">
            <div class="text-center">
                <div class="text-2xl font-bold text-blue-400">2+</div>
                <div class="text-blue-200 text-sm">Projects</div>
            </div>
            <div class="text-center">
                <div class="text-2xl font-bold text-blue-400">2+</div>
                <div class="text-blue-200 text-sm">Years of Learning</div>
            </div>
            <div class="text-center">
                <div class="text-2xl font-bold text-blue-400">3+</div>
                <div class="text-blue-200 text-sm">Clients</div>
            </div>
            </div>
            </div>



            <!-- Image -->
             <div class="lg:h-full flex justify-center lg:justify-end mt-15 relative">
                <div class="relative w-full max-w-md lg:max-w-lg">
                    <div class="relative z-10 bg-linear-to-r
                    from-blue-600 to-teal-600
                    rounded-[50%_40%_30%_60%/60%_40%_60%_30%]
                    p-4 backdrop-blur-sm border border-teal-500/30
                    -translate-y-6"
                    data-aos="zoom-in" data-aos-delay="500"
                    >
                    <div class="rounded-xl overflow-hidden">
                        <img src="/src/assets/minmin.png" alt="Hehe"
                        loading="lazy"
                        class="w-[500px] h-[600px] object-contain
                        -translate-y-8">
                    </div>
                </div>
                <div class="absolute -top-2 -right-4 w-10 h-10
                bg-blue-400 rounded-full blur-sm opacity-6
                animate-pulse"></div>
                </div>
        </div>
    </div>
    </section>

</template>

<style scoped>
</style>

