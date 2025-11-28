<script setup>
import { ArrowDownTrayIcon, 
         ArrowRightIcon, 
         BookOpenIcon, 
         ChatBubbleLeftRightIcon, 
         CodeBracketIcon, 
    EyeIcon } from '@heroicons/vue/16/solid';

import { ref } from 'vue';


const assetUrl = (path) => new URL(path, import.meta.url).href;

const projects = ref([
    {
        id: 1,
        title: "포트폴리오 웹사이트",
        desc: `Vue 와 Tailwind CSS를 사용하여 
        저의 이력을 간편하게 모아볼 수 있는 반응형 웹페이지를 작업하였습니다 반응형 컴포넌트들을 사용해서
        시각적 흥미도를 높이고, 방문하신 분들이 콘텐츠에 좀더 오래 집중할 수 있도록 작업했습니다
        `,
        image: assetUrl('@/project1.jpg'),
        category: 'Portfolio',
        bordColor: "border-blue-500/20",
        badgColor: "bg-cyan-500",
        technolg: [
            {
                name: "Vue.js",
                class: 'bg-blue-500/20 border-blue-400/30 text-blue-200'
            },
            {
                name: "Tailwind CSS",
                class: 'bg-cyan-500/20 border-cyan-400/30 text-cyan-200'
            },
            {
                name: "AOS",
                class: 'bg-blue-500/20 border-blue-400/30 text-blue-200'
            },
        ],
        links: [
            {
                name: "Live Demo", url: "#", icon: EyeIcon, type: "href",
                class: 'text-blue-400 hover:text-blue-300'
            },
            {
                name: "Code", url: "https://github.com/hogfather00/pofo.git", icon: CodeBracketIcon, type: "external",
                class: 'text-cyan-400 hover:text-cyan-300'
            },

        ]
    },
    {
        id: 2,
        title: "Java Spring & Brity RPA를 사용한 자동화 구현",
        desc: `Java Spring 을 사용하여 모의 COSTCO 물류관리 앱을 개발하고, 
               프론트에 해당 웹페이지를 연동하여 구동하였습니다. 페이지가 완성되고 난 후에는
               Brity RPA를 사용하여 자동화를 진행해 보았습니다
               `,
        image: assetUrl('@/project2.jpg'),
        category: 'Full-Stack',
        bordColor: "border-cyan-500/20",
        badgColor: "bg-blue-500",
        technolg: [
            {
                name: "Java",
                class: 'bg-blue-500/20 border-blue-400/30 text-blue-200'
            },
            {
                name: "Spring",
                class: 'bg-cyan-500/20 border-cyan-400/30 text-cyan-200'
            },
            {
                name: "OracleDB",
                class: 'bg-blue-500/20 border-blue-400/30 text-blue-200'
            },
        ],
        links: [
            {
                name: "Presentation", url: `https://docs.google.com/uc?export=download&id=1L_EOrXfWIZpKmv387DDe0zSZv3EXJCyI
`, icon: ArrowDownTrayIcon, type: "download",
                class: 'text-blue-400 hover:text-blue-300'
            },
        ]
    },
    {
        id: 3,
        title: "일정관리 앱",
        desc: `Vue와 반응형 웹을 사용한 간단한 일정관리 웹앱을 작업하였습니다.
        필터를 사용해서 해야 할 일, 완료한 일을 반응형 웹으로 실시간으로 표기할 수 있도록
        했습니다
        `,
        image: assetUrl('@/project3.jpg'),
        category: 'Portfolio',
        bordColor: "border-cyan-500/20",
        badgColor: "bg-cyan-500",
        technolg: [
            {
                name: "Vue.js",
                class: 'bg-cyan-500/20 border-cyan-400/30 text-cyan-200'
            },
            {
                name: "CSS",
                class: 'bg-blue-500/20 border-blue-400/30 text-blue-200'
            },
        ],
        links: [
            {
                name: "Code", url: "https://github.com/hogfather00/tasks-app", icon: CodeBracketIcon, type: "external",
                class: 'text-cyan-400 hover:text-cyan-300'
            },

        ]
    },
    {
        id: 4,
        title: "전시회 자료 번역 및 논문 초록 번역",
        desc: `석사 논문의 초록의 번역작업을 진행했으며, 국제 전시회에 참가할 때,
        홍보자료, 전시회 사용 자료들의 번역작업을 진행하고, 전시회에 참가하여 바이어들과
        계약이 잘 성사될 수 있도록 소통을 담당했습니다 `,
        image: assetUrl('@/project4.jpg'),
        category: 'Translation',
        bordColor: "border-blue-500/20",
        badgColor: "bg-blue-500",
        technolg: [
            {
                name: "English",
                class: 'bg-blue-500/20 border-blue-400/30 text-blue-200'
            },
            {
                name: "Korean",
                class: 'bg-cyan-500/20 border-cyan-400/30 text-cyan-200'
            },


        ],
        links: [
            {
                name: "Thesis", url: "https://dl.nanet.go.kr/search/searchInnerDetail.do?searchType=INNER_SEARCH&resultType=INNER_SEARCH_DETAIL&searchMehtod=L&searchClass=S&controlNo=KDMT12024000019259&queryText=&prevQueryText=김지은%3AAUTHOR%5EAUTHOR_WS%5EDP_AUTHOR_WS%3AAND%40숙명여자대학교%3APUB%5EPUB_WS%5EDP_PUB_WS%3AAND&zone=&fieldText=&prevPubYearFieldText=&languageCode=&synonymYn=&refineSearchYn=&ddcPopSearchYn=&pageNum=&pageSize=&orderBy=&topMainMenuCode=ALL&topSubMenuCode=&totalSize=33&totalSizeByMenu=33&seqNo=&hanjaYn=Y&knowPub=&isdb=&isdbsvc=&tt1=&down=&frgnLangMtrlYn=&targetLangCode=&checkedDbIdList=&baseDbId=&selectedDbIndexIdList=&caller=&asideState=&dpBranch=ALL&journalKind=&searchQuery=김지은+숙명여자대학교", icon: BookOpenIcon,
                type: "external" ,class: 'text-blue-400 hover:text-blue-300'
            },
            {
                name: "Abstract", url: "Thesis_Abstract.pdf", icon: ArrowDownTrayIcon,
                type: "download",class: 'text-blue-400 hover:text-blue-300'
            },

        ]
    },

])

</script>

<template>
    <section class="relative py-20 overflow-hidden" id="projects">
        <div class="relative z-10 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            
            <!-- Section Header -->
             <div class="text-center mb-16" data-aos="fade-up">
                <h2 class="text-4xl md:text-5xl font-bold text-white mb-4">
                   My <span class="text-transparent bg-clip-text
                   bg-linear-to-r from-blue-400 to-cyan-400">
                    Projects
                   </span> 
                </h2>

                <p class="text-blue-200 text-lg max-w-2xl mx-auto">
                    진행했던 업무와 프로젝트들을 간략하게 살펴보실 수 있습니다
                </p>
             </div>

             <!-- Projects Grid -->

             <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 gap-8">
                <div 
                v-for="(project, index) in projects"
                :key="(project.id)"
                class="group relative bg-linear-to-br from gray-800/50
                to-blue-900/30 rounded-3xl overflow-hidden border
                backdrop-blur-sm hover:border-blue-400/40
                transition-all duration-500 hover:transform 
                hover:-translate-y-2"
                :class="project.bordColor"
                data-aos="fade-up"
                :data-aos-delay="(index + 1) * 100">

                <!-- Project Image -->
                 <div class="relative overflow-hidden">
                    <img 
                    :src="project.image"
                    :alt="project.title"
                    class="w-full h-48 object-cover group-hover:scale-110 
                    transition-transform duration-500">
                    <div class="absolute inset-0 bg-linear-to-t
                    from-gray-900 via-transparent to-transparent
                    "></div>
                    <div class="absolute top-4 right-4">
                        <span class="px-3 py-1 text-white text-xs
                        rounded-full font-semibold"
                        :class="project.badgColor"
                        >
                            {{ project.category }}
                        </span>
                    </div>
                 </div>

                 <!-- Project Content -->

                 <div class="p-6">
                    <h3
                    class="text-xl font-bold text-white
                    group-hover:text-blue-400 transition-colors
                    duration-300"
                    > {{ project.title }}</h3>
                    <p class="text-blue-100 text-sm leading-relaxed mb-4">
                        {{ project.desc }}
                    </p>

                    <!-- Technologies -->

                    <div class="flex flex-wrap gap-2 mb-4">
                        <span
                        v-for="tech in project.technolg"
                        :key="tech"
                        class="px-2 py-1 border rounded text-xs"
                        :class="tech.class"
                        >{{ tech.name }}
                    </span>
                    </div>
                    <!-- Project Links -->

                    <div class="flex gap-3">
                        <a 
                        v-for="link in project.links"
                        :key="link.name"
                        :href="link.url"
                        :target="link.type === 'external' ? '_black' : null"
                        :class="link.class"
                        class="flex items-center gap-2 transition-colors 
                        duration-300 text-sm font-medium
                        ">
                        <component :is="link.icon" class="w-4 h-4" />
                            {{ link.name }}
                        
                        </a>
                    </div>
                 </div>
                </div>
             </div>

             <!-- CTA Section -->
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

