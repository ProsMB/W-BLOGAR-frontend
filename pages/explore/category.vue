<template>
<section>
    <div>
        <div class="bg-gray-600 w-5/6 h-96 m-auto mb-10">
        <img class="w-full h-full" src="https://greatpeopleinside.com/wp-content/uploads/2017/05/HR-GR8-technology.jpg" alt="">
        <div class="absolute top-80 lg:left-96 left-20 text-white">
            <li class="text-red-600 -mt-5 mb-5">Technology</li>
            <span class="font-bold lg:text-2xl underline">Lead your life a modern technology</span>
            <h1 class="font-bold lg:text-2xl underline">Provided all information relate to technology</h1>
        </div>
        </div>
        <div class="grid grid-cols-1 justify-center w-8/12 border-black m-auto">
            <blog-card v-for="i in 6" :key="i" />
        </div>
        <pagination/>
    </div>
</section>
</template>

<script>
import blogCard from '~/components/blogCard.vue'
import Pagination from '~/components/pagination.vue'
export default {
  components: { blogCard, Pagination },
    layout: 'layout',

}
</script>

<style>

</style>
