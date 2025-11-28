<script setup>
import { EnvelopeIcon, 
         MapPinIcon, 
         PhoneIcon
        } from '@heroicons/vue/16/solid';

</script>

<template>
    <section id="contact" class="py-32 text-center">
        <h2 class="text-4xl md:text-5xl font-bold text-white mb-6">
            Contact 
            <span class="text-transparent bg-clip-text bg-linear-to-r
            from-blue-400 to-cyan-400"> Info</span>
        </h2>

        <p class="text-white text-lg mb-10 font-semibold">
            함께 즐겁게 일할 수 있기를 고대하겠습니다.
        </p>

        <div class="mx-auto max-w-xl p-8 rounded-2xl bg-linear-to-r from-blue-600/20
        to-cyan-600/20 border border-blue-400/30 baackdrop-blur-sm shadow-xl">
        <div class="space-y-6 text-center">
            <div class="flex justify-center items-center gap-3"
            data-aos="fade-right"
            data-aos-delay="100"
            >
                <EnvelopeIcon class="w-6 h-6 text-blue-400" />
                <p class="text-white text-lg font-semibold">MoominKim@min.dev</p>
            </div>

            <div class="flex justify-center items-center gap-3"
            data-aos="fade-right"
            data-aos-delay="300"
            >
                <PhoneIcon class="w-6 h-6 text-blue-400" />
                <p class="text-white text-lg font-semibold">(+82) 010 3491 6660</p>
            </div>
            <div class="flex justify-center items-center gap-3"
            data-aos="fade-right"
            data-aos-delay="500"
            >
                <MapPinIcon class="w-6 h-6 text-blue-400" />
                <p class="text-white text-lg font-semibold"> Republic of Korea </p>
            </div>
        </div>
        </div>

    </section>
</template>

<style scoped>
</style>