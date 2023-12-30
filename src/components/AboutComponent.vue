<template>
    <div id="about" class="min-h-screen"  :class="isDark ? 'dark bg-gradient-to-br from-gray-800 via-gray-900 to-indigo-950 h-full' : 'bg-slate-200 text-black'" >
        <div class="flex flex-col gap-9 items-center w-5/6 mx-auto py-5">
            <div class="py-3">
                <h3 class="text-5xl font-bold my-2" :class="isDark ? 'dark text-slate-300' : 'text-slate-700'">Sobre mi.</h3>
                <p class=" text-pretty">Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio rerum qui reprehenderit. Numquam sunt hic velit autem eligendi vero, facilis in ullam, adipisci eius non aut rem suscipit, eum eveniet nulla amet cum! Repudiandae veritatis eum ad sapiente, quia, eveniet et, recusandae at doloremque modi quidem? Hic perferendis quos vero facilis inventore dignissimos sunt deleniti aliquid iure, quasi expedita quidem excepturi consequuntur nihil ipsa natus? Fugiat laboriosam expedita numquam optio consequuntur, commodi enim a ipsam sunt maxime impedit, laudantium mollitia maiores dicta ullam, earum natus inventore esse repellat suscipit. Accusamus facilis obcaecati aliquid sint magnam. Laudantium assumenda obcaecati delectus libero, deleniti quam reiciendis eos ducimus. Labore aspernatur, dolore quidem sequi laudantium perspiciatis placeat et velit voluptatibus libero distinctio dolor laboriosam tempora ullam error cupiditate harum? Cupiditate, eveniet. Animi delectus vel corporis doloribus, iure, nam laborum ex voluptates quod, architecto porro autem quasi adipisci pariatur ad dignissimos laudantium vitae obcaecati illo.</p>
            </div>

            <div class="flex flex-col md:flex-row py-5">
                <div class="py-5">
                    <h3 class="my-2 font-bold text-2xl">Educacion</h3>
                    <ul class="list-disc flex flex-wrap gap-5 flex-row">
                        <li v-for="tec in data" :key="tec.id" class="ml-5 text-xl font-bold">
                            {{tec.name}}
                            <span class="text-base block text-gray-500">{{tec.carrer}}
                                <span class="block text-gray-500">{{ tec.year }}</span>
                            </span>
                        </li>
                       
                    </ul>
                </div>



                <div class="py-5">
                    <h3 class="my-2 font-bold text-2xl">Tecnologias</h3>
                    <div class="flex flex-wrap gap-6 items-center ">

                        <div  class="flex flex-col items-center">
                            <img class="w-12 h-12" src="../assets/icons/python.svg" alt="python">
                            <p class="text-base block text-gray-500 text-center font-bold">Python</p>
                        </div>

                        <div  class="flex flex-col items-center">
                            <img class="w-12 h-12" src="../assets/icons/html.svg" alt="html">
                            <p class="text-base block text-gray-500 text-center font-bold">HTML</p>
                        </div>

                        <div  class="flex flex-col items-center">
                            <img class="w-12 h-12" src="../assets/icons/css.svg" alt="css">
                            <p class="text-base block text-gray-500 text-center font-bold">CSS</p>
                        </div>

                        <div class="flex flex-col items-center">
                            <img class="w-12 h-12" src="../assets/icons/javascript.svg" alt="Javascript">
                            <p class="text-base block text-gray-500 text-center font-bold">Javascript</p>
                        </div>
                        <div class="flex flex-col items-center">
                            <img class="w-12 h-12" src="../assets/icons/sql.svg" alt="SQL">
                            <p class="text-base block text-gray-500 text-center font-bold">SQL</p>
                        </div>

                        <div  class="flex flex-col items-center">
                            <img class="w-12 h-12" src="../assets/icons/vue.svg" alt="vue">
                            <p class="text-base block text-gray-500 text-center font-bold">Vue</p>
                        </div>

                        <div  class="flex flex-col items-center">
                            <img class="w-12 h-12" src="../assets/icons/tailwind.svg" alt="tailwind">
                            <p class="text-base block text-gray-500 text-center font-bold">Tailwind</p>
                        </div>

                        <div  class="flex flex-col items-center">
                            <img class="w-12 h-12" src="../assets/icons/git.svg" alt="git">
                            <p class="text-base block text-gray-500 text-center font-bold">Git</p>
                        </div>

                        <div  class="flex flex-col items-center">
                            <img class="w-12 h-12" src="../assets/icons/github.svg" alt="github">
                            <p class="text-base block text-gray-500 text-center font-bold">GitHub</p>
                        </div>


                    </div>

                </div>


            </div>


        </div>

    </div>
</template>

<script setup>
import { ref,computed } from 'vue';
import { educacion } from '../data/education';

const data = ref(educacion)

const emit = defineEmits([
    'darkMode'
])

const props = defineProps({
    dark:{
        type : Boolean
    }
})

const isDark = computed(() => {
    return props.dark;
})

</script>

<style scoped></style>