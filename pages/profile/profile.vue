<template>
<section>
    <div class="bg-gray-600 w-5/6 h-96 m-auto mb-24">
        <div class="grid grid-rows-2 bg-white h-72 w-72 h z-50 absolute top-64 top left-24 lg:left-60 rounded-xl border-none shadow-xl">
            <div class="w-full h-full grid bg-slate-300 rounded-tl-xl rounded-tr-xl">
                <img class="rounded-full h-32 w-32 m-auto" src="https://alrigh.com/wp-content/uploads/2020/06/10-Midoriya-Izuku-profile-picture-1024x1018.jpg" alt="">
            </div>
            <div class="w-full h-full grid grid-rows-4">
                <div class="inline-flex mt-2 space-x-2 pl-4">
                    <svg class="w-4 h-4 mt-0.5 text-gray-500 hover:text-black" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z"></path>
                    </svg>
                    <p class="text-sm">: Jonathan Reinink</p>
                </div>
                <div class="inline-flex -mt-2 space-x-2 pl-4">
                    <svg class="w-4 h-4 mt-1 text-gray-500 hover:text-black" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path>
                    </svg>
                    <p class="text-sm">: jonathan.reinink@gmail.com</p>
                </div>
                <div class="inline-flex -mt-6 space-x-2 pl-4">
                    <svg class="w-4 h-4 mt-1 text-gray-500 hover:text-black" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                        <path d="M12 14l9-5-9-5-9 5 9 5z"></path>
                        <path d="M12 14l6.16-3.422a12.083 12.083 0 01.665 6.479A11.952 11.952 0 0012 20.055a11.952 11.952 0 00-6.824-2.998 12.078 12.078 0 01.665-6.479L12 14z"></path>
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 14l9-5-9-5-9 5 9 5zm0 0l6.16-3.422a12.083 12.083 0 01.665 6.479A11.952 11.952 0 0012 20.055a11.952 11.952 0 00-6.824-2.998 12.078 12.078 0 01.665-6.479L12 14zm-4 6v-7.5l4-2.222"></path>
                    </svg>
                    <p class="text-sm">: Software Engineer</p>
                </div>
                <media-icon/>
            </div>
        </div>
    </div>
    <div class="flex justify-end items-center mx-12 md:mx-40">
        <button class="rounded-full flex items-center border-blue-400 border-2 hover:bg-blue-400 text-blue-400 hover:text-white transform hover:scale-95 transition ease-in-out duration-500" @click="newBLog">
             <span class="inline-block px-1 md:px-3 py-1 text-sm font-semibold -mt-1 md:mt-1 md:mb-2 pt-2">Add Your Blog</span>
             <svg class="w-7 h-7 inline md:-ml-2 mr-1 md:mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 9v3m0 0v3m0-3h3m-3 0H9m12 0a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
        </button>
    </div>
    <form-blog-post v-show="blogForm" @closeForm="closeForom" @createBlog="createBLog"/>
    <div class=" mt-12 w-24 h-8 text-center border-blue-600 text-white bg-gray-600 ml-32 text-lg font-semibold rounded-tl-lg rounded-tr-lg">All Blogs</div>
    <div class="grid lg:grid-cols-4 md:grid-cols-3 sm:grid-cols-1 gap-6 border-t-2 border-gray-600 mx-32">
       <blog-card-user v-for="i in 8" :key="i"/>
    </div>
    <pagination/>
</section>
</template>

<script>
import pagination from '~/components/pagination.vue';
import blogCardUser from '~/components/blogCardUser.vue';
import mediaIcon from '~/components/mediaIcon.vue';
import FormBlogPost from '~/components/formBlogPost.vue';
export default {
    components:{pagination,blogCardUser,mediaIcon, FormBlogPost},
    layout: 'layout',
    data() {
        return {
            blogForm : false,
        }
    },
    methods:{
        newBLog(){
            this.blogForm = true;
        },
        closeForom(toggle){
            this.blogForm = toggle;
        },
        createBLog(toggle){
            this.blogForm = toggle;
        }
    }
}
</script>

<style>

</style>
