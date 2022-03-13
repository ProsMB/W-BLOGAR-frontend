<template>
  <section>
      <div class="h-full w-full opacity-50 bg-gray-900 z-[60] fixed top-0 left-0 m-auto"></div>
            <div class="bg-white  w-8/12 z-[111] fixed -ml-1 top-24 bottom-24 left-80 p-3 rounded-xl">
                <div class="w-full flex justify-end border-b-2 cursor-pointer">
                    <svg class="w-7 h-7 transform hover:scale-95 duration-300 z-[80]" @click="closeComment" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 14l2-2m0 0l2-2m-2 2l-2-2m2 2l2 2m7-2a9 9 0 11-18 0 9 9 0 0118 0z"></path>
                    </svg>
                </div>
                <div class="h-full w-full">
                    <div class=" h-5/6 overflow-y-auto">
                        <comment-card v-for="i in 7" :key="i"/>
                    </div>
                    <div class="h-1/6 flex items-center w-11/12 m-auto -mt-2 rounded-xl">
                        <textarea class="resize-none rounded-xl w-full outline-none -pb-4 border-r-2 bg-gray-200 px-3" type="text" placeholder="Leave your comment here"></textarea>
                        <button>
                            <svg class="w-6 h-6 mx-3 rotate-90 transform hover:scale-95 " fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 19l9 2-9-18-9 18 9-2zm0 0v-8"></path>
                            </svg>
                        </button>
                    </div>
                </div>
            </div>
  </section>
</template>

<script>
import commentCard from '~/components/commentCard.vue'
export default {
    components:{commentCard},
    emits:['closeComment'],
    data(){
        return {
            
        }
    },
    methods:{
        closeComment(){
            this.$emit('closeComment',false);
        }
    }
}
</script>

<style>

</style>