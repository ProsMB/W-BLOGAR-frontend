<template>
<section>

    <div class="w-fulll h-2/6 grid grid-cols-4 gap-12 my-6">
        <nuxt-link to="/blogs/blog">

            <img class="lg:col-span-1 lg:block md:col-span-1 md:block hidden h-full w-full transform hover:scale-105 transition ease-in-out duration-500" src="https://imageio.forbes.com/specials-images/imageserve/5ef3f7eec4f2390006f0c356/GUI--Graphical-User-Interface--concept-/960x0.jpg?fit=bounds&format=jpg&width=960" alt="Sunset in the mountains">
        </nuxt-link>

        <div class="col-span-4 lg:col-span-3 md:col-span-3 border-b border-gray-400 lg:border-gray-400 bg-white p-3 flex flex-col justify-between leading-normal link-underline link-underline-black">
            <div>
                <p class="text-sm text-blue-800 flex items-center">
                    <svg class="w-6 h-6 text-black mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9"></path>
                    </svg>
                    Technology
                </p>
                <p class="text-sm text-gray-500">August 18, 2022</p>
                <nuxt-link to="/blogs/blog">
                    <div class="text-gray-900 font-semibold text-xl mb-2 font-sans">Can coffee make you a better developer?</div>
                    <p class="text-gray-700 text-base">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium nihil.</p>
                </nuxt-link>

            </div>
            <div class="flex items-center justify-between">
                <nuxt-link to="/profile/other">

                    <div class="flex items-center">
                        <img class="w-10 h-10 rounded-full mr-4" src="https://alrigh.com/wp-content/uploads/2020/06/10-Midoriya-Izuku-profile-picture-1024x1018.jpg" alt="Avatar of Jonathan Reinink">
                        <div class="text-sm mt-1">
                            <p class="text-gray-900 leading-none">Jonathan Reinink</p>
                            <div class="mt-1 -ml-1">
                                <svg class="w-6 h-6 text-gray-500 inline -mt-1.5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                    <path d="M12 14l9-5-9-5-9 5 9 5z"></path>
                                    <path d="M12 14l6.16-3.422a12.083 12.083 0 01.665 6.479A11.952 11.952 0 0012 20.055a11.952 11.952 0 00-6.824-2.998 12.078 12.078 0 01.665-6.479L12 14z"></path>
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 14l9-5-9-5-9 5 9 5zm0 0l6.16-3.422a12.083 12.083 0 01.665 6.479A11.952 11.952 0 0012 20.055a11.952 11.952 0 00-6.824-2.998 12.078 12.078 0 01.665-6.479L12 14zm-4 6v-7.5l4-2.222"></path>
                                </svg>
                                <p class="inline text-sm text-gray-500">Engineer</p>

                            </div>
                        </div>
                    </div>
                </nuxt-link>

                <div class="grid grid-cols-3 items-center gap-4">
                    <div>
                        <svg class="w-8 h-8 mt-6 cursor-pointer" v-show="!like" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" @click="Islike">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"></path>
                        </svg>
                        <svg class="w-8 h-8 mt-6" v-show="like" fill="red" stroke="red" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" @click="Islike">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"></path>
                        </svg>
                        <p>1k</p>
                    </div>
                    <div @click="openComment">
                        <svg class="w-6 h-6 mt-6 cursor-pointer" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 10h.01M12 10h.01M16 10h.01M9 16H5a2 2 0 01-2-2V6a2 2 0 012-2h14a2 2 0 012 2v8a2 2 0 01-2 2h-5l-5 5v-5z"></path>
                        </svg>
                        <p>200</p>
                    </div>
                    <div>
                        <svg class="w-6 h-6 mt-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"></path>
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z"></path>
                        </svg>
                        <p>1,5K</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div v-show="commentModal">
        <comment-modal @closeComment="closeComment" />
    </div>
</section>
</template>

<script>
import commentModal from '~/components/commentModal.vue';
export default {
    components:{commentModal},
    data() {
        return {
            commentModal:false,
            like: false,
        }
    },
    methods: {
         openComment() {
            this.commentModal = true;
        },
        closeComment(toggle) {
            this.commentModal = toggle;
        },
        Islike() {
            this.like = !this.like;
        }
    }

}
</script>

<style>

</style>
