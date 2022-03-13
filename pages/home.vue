<template>
<section>
    <div class="h-80 w-full bg-slate-200 m-auto flex items-end justify-center -z-50">
        <div v-for="category in categories" :key="category.name">
            <nuxt-link to="explore/category">
                <div class="h-48 w-48 mx-6 mb-10 transform hover:scale-105 transition ease-in-out duration-500">
                    <img class="h-full w-full rounded-2xl outline-none" :src="category.imgurl" alt="categoryType">
                    <p class="text-white relative -top-14 text-center font-semibold text-lg">{{category.name}}</p>
                </div>
            </nuxt-link>
        </div>
    </div>

    <!-- blog card -->

    <div class="grid grid-cols-1 border-black mx-28">
        <blog-card v-for="i in 6" :key="i" />
    </div>

    <!-- Pagination -->

    <pagination/>
</section>
</template>

<script lang="ts">
import Vue from 'vue'
import blogCard from '~/components/blogCard.vue'
import Pagination from '~/components/pagination.vue'
export default Vue.extend({
    layout: 'layout',
    components: {
        blogCard,
        Pagination
    },
    data() 
        {
        return {
            categories: [{
                    name: "Technology",
                    imgurl: "https://greatpeopleinside.com/wp-content/uploads/2017/05/HR-GR8-technology.jpg"
                },
                {
                    name: "Travel",
                    imgurl: "https://ntvb.tmsimg.com/assets/p21390197_b_h8_aa.jpg?w=960&h=540"
                },
                {
                    name: "Food",
                    imgurl: "https://i.guim.co.uk/img/media/a6795e6f75daa968c1154d4acedc091599c98474/0_299_4973_2984/master/4973.jpg?width=1200&quality=85&auto=format&fit=max&s=b641084777d2dedffc4dc6523078514d"
                },
                {
                    name: "Creative",
                    imgurl: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTK-i2oXZg7LQILuR6lwFBu-bcPANjEXMq68Q&usqp=CAU"
                },
                {
                    name: "Life Style",
                    imgurl: "https://www.apa.org/images/lifestyle-changes-title-image_tcm7-211644.jpg"
                },
                {
                    name: "Sharing",
                    imgurl: "https://kasperspiro.com/wp-content/uploads/2016/10/knowledge-sharing.jpg"
                }
            ]
        }
    }
})
</script>

<style scoped>

</style>
