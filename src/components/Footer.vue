<script setup>
import { EnvelopeIcon, MapPinIcon, PhoneIcon } from '@heroicons/vue/24/outline';


const quickLinks = [
    { name: "Home", href: "#home" },
    { name: "About", href: "#about" },
    { name: "Services", href: "#services" },
    { name: "Projects", href: "#projects" },
    { name: "Contact", href: "#contact" },
]
</script>

<template>
    <footer class="relative bg-gray-900/80 border-t border-blue-500/20">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 py-12">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <!-- Brand -->
                 <div class="md:col-span-2">
                    <div class="text-2xl font-bold bg-linear-to-r
                    from-blue-400 to-teal-400 bg-clip-text
                    text-transparent mb-4
                    "> Min </div>
                 
                 <p class="text-blue-200 text-sm leading-relaxed max-w-md">
                    저의 포트폴리오를 방문해 주셔서 감사합니다
                    <br /> 누군가에게 도움이 되는 의미있는 것들을 만들기 위해,
                    <br /> 매일 조금씩 배워나가며 성장하고 있습니다.
                 </p>
                 <div class="flex gap-4 mt-6">
                    <a href="#contact" class="p-2 bg-blue-500/20 border
                    border-blue400/30 rounded-lg text-blue-400
                    hover:bg-blue-500/30 transition-all">
                    <EnvelopeIcon class="w-5 h-5" />
                </a>
                <a href="#contact"
                class="p-2 bg-blue-500/20 border
                    border-blue400/30 rounded-lg text-blue-400
                    hover:bg-blue-500/30 transition-all">
                    <PhoneIcon class="w-5 h-5" />
                </a>
                <a href="#contact"
                class="p-2 bg-blue-500/20 border
                    border-blue400/30 rounded-lg text-blue-400
                    hover:bg-blue-500/30 transition-all">
                    <MapPinIcon class="w-5 h-5" />
                </a>
                 </div>
                 </div>

                 <!-- Quick Links -->
                  <div>
                    <h3 class="text-white font-semibold mb-4">
                        Quick Links
                    </h3>
                    <ul class="space-y-2">
                        <li
                        v-for="link in quickLinks"
                        :key="link.name"
                        class="text-blue-200 hover:text-blue-400
                        text-sm transition-colors">
                        <a 
                        :href="link.href"
                        class="text-blue-200 hover:text-blue-400 text-sm transition-colors"   
                        >
                        {{ link.name }}
                        </a>
                        </li>
                    </ul>
                  </div>

                  <!-- Services -->
                    <div class="flex flex-col gap-3 mt-4 rotate-180">
                        <div class="w-24 h-[4px] bg-linear-to-r from-blue-500 to-cyan-400 rounded-full"></div>
                        <div class="w-16 h-[4px] bg-linear-to-r from-cyan-400 to-teal-400 rounded-full"></div>
                        <div class="w-32 h-[4px] bg-linear-to-r from-blue-600 to-teal-500 rounded-full"></div>
                    </div>
            </div>
            <!-- Bottom Bar -->
             <div class="border-t border-blue-500/20 mt-8 pt-8 flex
             flex-col md:flex-row justify-between items-center
             ">
             <p class="text-blue-300 text-sm">
                @ 2025 Min. All rights reserved
             </p>
             <div class="flex gap-6 mt-4 md:mt-0">
                <a href="#" class="text-blue-400 text-sm transition-colors">
                    Privacy Policy
                </a>
                <a href="#" class="text-blue-400 text-sm transition-colors">
                    Terms of Service
                </a>
             </div> 
            </div>
        </div>
    </footer>
</template>

<style scoped>
</style>