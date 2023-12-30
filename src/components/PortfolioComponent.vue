<template>
    <div id="portfolio" class="py-5 min-h-screen" :class="isDark ? 'dark bg-slate-900' : 'text-black bg-slate-300'">
        <h2 class="text-5xl font-semibold text-center" :class="isDark ? 'dark text-slate-300' : 'text-slate-700'">Portfolio
        </h2>

        <div class="grid mt-5 md:grid-cols-2 md:gap-3 lg:grid-cols-3 p-4 w-5/6 mx-auto"
            :class="isDark ? 'dark' : 'text-black'">

            <div class="rounded-lg shadow-2xl overflow-hidden my-4"
                :class="isDark ? 'dark shadow-blue-900/30' : 'text-black bg-white'" v-for="item in data" :key="item.id">
                <div class=" h-30">
                    <img class="h-full w-full object-fill object-center" :src=item.image :alt=item.title loading="lazy">
                    <div class="flex flex-col p-6">
                        <div class="space-y-2">
                            <h3 class="text-xl font-semibold text-sky-500">{{ item.title }}</h3>
                            <p>{{ item.description }}</p>
                        </div>
                        <div class=" flex justify-center space-x-10 my-5">
                            <a class="inline-block rounded bg-gradient-to-r from-green-400 to-blue-500 px-8 py-3 text-sm font-medium text-white transition hover:scale-110 hover:shadow-xl focus:outline-none focus:ring active:bg-indigo-500"
                                :href="item.live" target="_blank">
                                Live
                            </a>

                            <a class="inline-block rounded bg-gradient-to-r from-green-400 to-blue-500 px-8 py-3 text-sm font-medium text-white transition hover:scale-110 hover:shadow-xl focus:outline-none focus:ring active:bg-indigo-500"
                                :href="item.github" target="_blank">
                                Code
                            </a>
                        </div>
                    </div>

                </div>

            </div>
        </div>
    </div>
</template>

<script setup>
import { computed } from 'vue';

const emit = defineEmits([
    'darkMode'
])



const isDark = computed(() => {
    return props.dark;
})


const props = defineProps({
    data: {
        type: Object
    },
    dark: {
        type: Boolean
    }
})


</script>

<style scoped></style>