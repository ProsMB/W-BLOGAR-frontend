<template>
<section>
    <div>
        <div class="flex items-center w-8/12 m-auto mt-20 mb-5 shadow-lg rounded-xl">
            <input class="rounded-tl-xl rounded-bl-xl w-full p-3 outline-none border-r-2" type="text" placeholder="Type blog's title here">
            <button>
                <svg class="w-6 h-6 mx-3 transform hover:scale-95" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"></path>
                </svg>
            </button>
        </div>
    </div>
    <div class="grid grid-cols-1 justify-center w-8/12 border-black m-auto">
        <blog-card v-for="i in 6" :key="i"/>
    </div>
    <pagination/>
</section>
</template>

<script>
import blogCard from '~/components/blogCard.vue';
import Pagination from '~/components/pagination.vue';
export default {
    layout: 'layout',
    components:{blogCard, Pagination},


}
</script>

<style>

</style>
