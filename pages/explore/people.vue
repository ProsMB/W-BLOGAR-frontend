<template>
<section>
    <div>
        <div class="flex items-center w-8/12 m-auto my-10 shadow-lg rounded-xl">
            <input class="rounded-tl-xl rounded-bl-xl w-full p-3 outline-none border-r-2" type="text" placeholder="Type people's name here">
            <button>
                <svg class="w-6 h-6 mx-3 transform hover:scale-95" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"></path>
                </svg>
            </button>
        </div>
    </div>
    <div class="w-8/12 m-auto bg-gray-200 rounded-lg hover:opacity-80" v-for="i in 8" :key="i">
        <user-card/>
    </div>
    <pagination/>
</section>
</template>

<script>
import Pagination from '~/components/pagination.vue'
import userCard from '~/components/userCard.vue'
export default {
  components: { userCard, Pagination },
    layout: 'layout',

}
</script>

<style>

</style>
