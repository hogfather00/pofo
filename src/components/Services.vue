<script setup>
import { ref } from 'vue';
import { ArrowRightIcon, 
        BuildingStorefrontIcon, 
        CodeBracketIcon,
        Cog8ToothIcon, 
        DocumentTextIcon,
        GlobeAltIcon, 
        PaintBrushIcon } from '@heroicons/vue/16/solid';

const services = ref([
    {
    id: 1,
    icon: CodeBracketIcon,
    name: 'Web Development',
    desc: `Java, Python, JavaScript 기반의 웹 서비스 개발 경험과 Vue, Spring, Flask 등 현대적인 프레임워크를 다룰 수 있습니다`
    },
    {
    id: 2,
    icon: DocumentTextIcon,
    name: 'Document Writing',
    desc: `오피스 도구와 프레젠테이션 작성에 능숙하며, 목적과 대상에 맞는 명확한 문서를 작성할 수 있습니다`
    },
    {
    id: 3,
    icon: Cog8ToothIcon,
    name: 'Workflow Automation',
    desc: `API와 Python 기반 자동화 시스템을 구축하여 반복 업무 시간을 효율적으로 단축한 경험이 있습니다`
    },
    {
    id: 4,
    icon: GlobeAltIcon,
    name: 'Business English',
    desc: `업무 커뮤니케이션 및 문서/이메일 작성에 능숙하며 영문 자료 번역 및 실무 영어 소통 경험이 다수 있습니다`
    },
    {
     id: 5,
    icon: PaintBrushIcon,
    name: 'Illust Design',
    desc: `벡터 기반 일러스트레이션 제작 및 UI 요소 디자인 경험이 있습니다`
    }, 
    {
     id: 6,
    icon: BuildingStorefrontIcon,
    name: 'E-commerce Merchandise',
    desc: `전자상거래 플랫폼의 운영 및 상품 등록/관리 프로세스를 이해하며 다양한 판매 채널 경험을 보유하고 있습니다`
    },
])

</script>

<template>
    <section class="relative py-20 overflow-hidden" id="services">
        <div class="relative z-10 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center m-16" data-aos="fade-up">
                <h2 class="text-4xl md:text-5xl font-bold text-white mb-4">
                    My 
                    <span class="text-transparent bg-clip-text bg-linear-to-r
                    from-blue-400 to-cyan-400
                    ">Services</span>
                </h2>

                <p class="text-blue-200 text-lg max-w-2xl mx-auto"
                data-aos="fade-up"
                data-aos-delay="100">
                    매일 누군가에게 도움이 되는 것들을 만들기 위해 새로운 것을 배우고 실현합니다
                </p>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div
                v-for="(service, index) in services"
                :key="service.id"
                :data-aos="'fade-up'"
                :data-aos-delay="(index * 100) + 200"
                class="group relative p-8 rounded-2xl bg-linear-to-br
                from-gray-800/50 to-blue-900/30 backdrop-blur-sm
                border border-blue-500/20 hover:border-blue-400/40
                transition-all duration-500 hover:transform
                hover:-translate-y-2
                "
                >
                <div class="absolute inset-0 bg-linear-t-r from-blue-500/5
                to-cyan-500/5 rounded-2xl opacity-0 duration-500
                group-hover:opacity-100 transition-opacity"></div>
                <div class="relative z-10 mb-6">
                    <div class="inline-flex items-center justify-center
                    w-16 h-16 rounded-xl bg-linear-to-r from-blue-500/20
                    to-cyan-500/20 border border-blue-400/30
                    group-hover:scale-110 transition-transform
                    duration-300
                    ">
                    <component
                    :is="service.icon"
                    class="w-8 h-8 text-blue-400"></component>
                </div>
                </div>
                <div class="relative z-10">
                    <h3 class="text-xl font-bold text-white mb-3
                    group-hover:text-blue-400 transition-colors
                    duration-300
                    ">{{ service.name }}</h3>
                    <p class="text-blue-100 leading-relaxed">
                        {{ service.desc }}
                    </p>
                </div>
                <div class="absolute bottom-6 right-6 opacity-0
                grouphover:opacity-100 transform translate-x-4
                group-hover:translate-x-0 transition-all duration-300
                ">
                <ArrowRightIcon class="w-6 h-6 text-cyan-400" />
            </div>
                </div>
            </div>
            <div
            class="w-full flex justify-center mt-30"
            data-aos="fade-up"
            data-aos-delay="500"
            >
            <div class="progress-line w-100 h-[5px] bg-linear-to-r from-blue-500 to-cyan-400 rounded-full"></div>
            
        </div>
        </div>
    </section>
</template>

<style scoped>
</style>