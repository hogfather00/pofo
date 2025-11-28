<script setup>
import { BookOpenIcon, 
         BriefcaseIcon, 
         CloudIcon, 
         CodeBracketIcon, 
         PaintBrushIcon, 
         ServerIcon, 
         Squares2X2Icon } from '@heroicons/vue/16/solid';


const skills = [
    {
        id: 1,
        title: "Frontend Development",
        icon: CodeBracketIcon,
        iconColor: 'text-blue-400',
        percentage: 68,
        percentageColor: "text-blue-400 text-sm",
        gradient: 'bg-linear-to-r from-blue-500 to-cyan-500'

    },
        {
        id: 2,
        title: "Backend Development",
        icon: ServerIcon,
        iconColor: 'text-blue-400',
        percentage: 85,
        percentageColor: "text-cyan-400 text-sm",
        gradient: 'bg-linear-to-r from-cyan-500 to-blue-500'

    },
        {
        id: 3,
        title: "UI/UX Design",
        icon: PaintBrushIcon,
        iconColor: 'text-blue-400',
        percentage: 70,
        percentageColor: "text-blue-400 text-sm",
        gradient: 'bg-linear-to-r from-blue-500 to-cyan-500'

    },
        {
        id: 4,
        title: "Documentation",
        icon: BookOpenIcon,
        iconColor: 'text-cyan-400',
        percentage: 90,
        percentageColor: "text-blue-400 text-sm",
        gradient: 'bg-linear-to-r from-cyan-500 to-blue-500'

    },
    {
        id: 5,
        title: "DevOps & Cloud",
        icon: CloudIcon,
        iconColor: 'text-blue-400',
        percentage: 75,
        percentageColor: "text-blue-400 text-sm",
        gradient: 'bg-linear-to-r from-blue-500 to-cyan-500'

    },
]

const experiences = [
    {
        id: 1,
        position: "General Manager",
        company: "Gaul Inc",
        period: "2024 - Present",
        desc: `사방넷 API를 활용하여 3000가지 정도 되는 상품을 각 채널별로 효율적으로 관리할 수 있도록 
        Python 자동화 코드를 작성했습니다 인사관리의 업무중 일부, 
        Shopby 기반 자사몰 유지보수와 디자인에 대한 업무도 함께 진행했습니다`,
        borderColor: "border-blue-500/30",
        dotColor: "bg-blue-500",
        borderClass: "border-blue-500/20",
        dateColor: "text-blue-400 text-sm font-semibold",
        companyColor: "text-cyan-400"
    },
        {
        id: 2,
        position: "Bartender",
        company: "Cunard / Carnival UK",
        period: "2022 - 2024",
        desc: `영국의 큐나드사의 크루즈선 퀸메리2호에서 바텐더로 근무하였습니다 
        선내의 8개의 모두 다른 컨셉의 바를 운영하고 
        직원 스케쥴, 재고 조정, 데일리 리포트 작성등 전반적인 운영을 맡아 진행했습니다`,
        borderColor: "border-cyan-500/30",
        dotColor: "bg-cyan-500",
        borderClass: "border-cyan-500/20",
        dateColor: "text-cyan-400 text-sm font-semibold",
        companyColor: "text-blue-400"
    },
            {
        id: 3,
        position: "Internation Sales Specialist",
        company: "Global Ez Inc",
        period: "2020 - 2022",
        desc: `해외영업 담당자로 해외에서 열리는 여러 전시회에 참가하였습니다
        디자이너와 협업하여 전시부스를 계획하고 전시회에 참석하여 제품을 해외 바이어들에게 소개하였으며
        전시회가 진행되는동안 일어나는 대부분의 일정을 조율하고 계약을 성사하는 업무를 진행했습니다
        `,
        borderColor: "border-blue-500/30",
        dotColor: "bg-blue-500",
        borderClass: "border-blue-500/20",
        dateColor: "text-blue-400 text-sm font-semibold",
        companyColor: "text-cyan-400"
    },
]

const techStack = [
    'Java', 'Spring', 'Python', 'Flask', 'Javascript', 'Vue', 'Tailwind CSS', 'Inkscape', 'Git', 'Docker', 'Rest APIs'
]
</script>

<template>
    <section class="relative py-20 overflow-hidden" id="skills">

        <div class="relative z-10 max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16" data-aos="fade-up">
                <h2 class="text-4xl md:text-5xl font-bold text-white mb-4">
                    <span class="text-transparent bg-clip-text bg-linear-to-r 
                    from-blue-400 to-cyan-400
                    ">
                        Skills
                    </span> & Experience
                </h2>
                <p class="text-blue-200 text-lg max-w-2xl mx-auto">
                    제가 가지고 있는 기술들과 전문성 그리고 경력들입니다
                </p>
            </div>

            <div class="grid lg:grid-cols-2 gap-12 lg:gap-16">
                <div data-aos="fade-right">
                    <h3 class="text-2xl font-bold text-white mb-8 flex
                    items-center gap-3
                    ">
                    Technical skills
                </h3>
                <div class="space-y-6">
                    <div
                    v-for="skill in skills"
                    :key="skill.id"
                    class="group"
                    >
                    <div class="flex items-center justify-between mb-3">
                        <span class="text-blue-200 font-semibold flex items-center gap-2">
                            <component
                            :is="skill.icon"
                            class="w-5 h-5"
                            :class="skill.iconColor"
                            >
                            {{ skill.title }}
                            </component>
                        </span>
                        <span :class="skill.percentageColor">
                            {{ skill.percentage }} %
                        </span>
                    </div>
                    <div class="h-2 bg-gray-700 rounded-full overflow-hidden">
                        <div class="h-full rounded-full transition-all duration-1000
                        group-hover:scale-105"
                        :class="skill.gradient"
                        :style="{width: skill.percentage + '%'}"
                        >

                        </div>
                    </div>
                </div>
                </div>
                    <div class="mt-12">
                    <h4 class="text-xl font-bold text-white mb-6 flex items-center gap-2">
                        <Squares2X2Icon class="w-6 h-6 text-cyan-400" />
                        Tech Stack
                    </h4>
                    <div class="flex flex-wrap gap-3">
                        <span
                        v-for="tech in techStack"
                        :key="tech"
                        class="px-4 py-2 bg-linear-to-r from-blue-500/20
                        border border-blue-400/30 rounded-full
                        text-blue-200 text-sm font-medium
                        hover:scale-105 transition-transform
                        duration-300
                        "
                        >{{ tech }}</span>
                    </div>
                </div>
                </div>
                <div data-aos="fade-left">
                    <h3 class="text-2xl font-bold text-white mb-8 
                    flex items-center gap-3">
                    <BriefcaseIcon class="w-8 h-8 text-cyan-400" />
                    Experiences
                    </h3>
                    <div class="space-y-8">
                        <div
                        v-for="exp in experiences"
                        :key="exp.id"
                        class="relative pl-8 border-l-2 group"
                        :class="exp.borderColor"
                        >
                        <div
                        class="absolute -left-2 top-0 w-4 h-4 rounded-full
                        group-hover:scale-150 transition-transform
                        duration-300"
                        :class="exp.dotColor">
                    </div>
                    <div class="bg-linear-to-br from-gray-800/50
                    to-blue-900/30 rounded-2xl p-6 border
                    backdrop-blur-sm group-hover:border-blue-400/40
                    transition-all duration-300"
                    :class="exp.borderClass">
                    <div class="flex flex-col sm:flex-row sm:items-center
                    sm:justify-between mb-3">
                    <h4 class="text-lg font-bold text-white">
                        {{ exp.position }}</h4>
                        <span
                        :class="exp.dateColor"
                        class="mt-1 sm:mt-0"
                        >{{ exp.period }}</span>
                </div>
                <p
                :class="exp.companyColor"
                class="font-medium mb-3"
                >{{ exp.company }}</p>
                <p
                class="text-blue-100 text-sm leading-relaxed"
                >{{ exp.desc }}</p>

                </div>
                    </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped>
</style>