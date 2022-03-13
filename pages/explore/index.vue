<template>
<div class="w-full text-white my-12">
    <div class=" mt-12 w-24 h-8 text-center border-gray-600 text-white bg-gray-600 ml-12 md:mx-36 lg:ml-48 text-lg font-semibold rounded-tl-lg rounded-tr-lg">Search For :</div>
    <hr class="border-t-2 border-gray-600 mx-12 md:mx-36 lg:mx-48">

    <div class="w-8/12 grid grid-cols-2 gap-12 m-auto bg-white my-8">
        <nuxt-link to="/explore/people">
            <div class="h-full w-full hover:opacity-75 hover:-translate-y-3 duration-500">
                <img class="h-full w-full rounded-2xl outline-none " src="https://fiverr-res.cloudinary.com/images/q_auto,f_auto/gigs/141968207/original/354c134911bc63caba814a801e5db046d8c62beb/help-you-in-sourcing-right-candidate-for-your-organization.jpg" alt="movie">
                <p class="text-white relative -top-20 text-center font-semibold text-2xl">People</p>
            </div>
        </nuxt-link>
        <nuxt-link to="/explore/blogs">
            <div class="h-full w-full hover:opacity-75 hover:-translate-y-3 duration-500">
                <img class="h-full w-full rounded-2xl outline-none" src="https://images.contentstack.io/v3/assets/bltefdd0b53724fa2ce/blt40f2fdc1e95deca0/618ab1474f03d166757397de/blog-thumb-website-search.png" alt="movie">
                <p class="text-white relative -top-20 text-center font-semibold text-2xl">Blogs</p>
            </div>
        </nuxt-link>
    </div>

    <div class=" mt-12 w-24 h-8 text-center border-gray-600 text-white bg-gray-600 ml-12 md:ml-36 lg:ml-48 text-lg font-semibold rounded-tl-lg rounded-tr-lg">Category :</div>
    <hr class="border-t-2 border-gray-600 mx-12 md:mx-36 lg:mx-48">
    <div class="w-8/12 grid grid-cols-3 gap-6 m-auto bg-white mt-6" >
        <div v-for="category in categories" :key="category.name">
            <nuxt-link to="/explore/category">
                <div class="h-full w-full transform hover:scale-105 transition ease-in-out duration-500">
                    <img class="h-full w-full rounded-2xl outline-none" :src="category.imgurl" alt="movie">
                    <p class="text-white relative -top-14 text-center font-semibold text-lg">{{category.name}}</p>
                </div>
            </nuxt-link>
        </div>
    </div>
</div>
</template>

<script>
export default {
    layout: 'layout',
    data() {
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
}
</script>

<style>

</style>
