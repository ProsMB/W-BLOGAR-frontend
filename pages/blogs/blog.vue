<template>
<section>
    <div class="py-12">
        <div class="w-8/12 m-auto">
            <li class="text-red-500">Technology</li>
            <h1 class="font-semibold text-xl my-3">Can coffee make you a better developer?</h1>
            <div class="flex items-center justify-between">
                <div class="flex items-center">
                    <nuxt-link to="/profile/other">

                        <img class="w-10 h-10 rounded-full mr-4" src="https://alrigh.com/wp-content/uploads/2020/06/10-Midoriya-Izuku-profile-picture-1024x1018.jpg" alt="Avatar of Jonathan Reinink">
                    </nuxt-link>

                    <div class="text-sm mt-1">
                        <nuxt-link to="/profile/other">
                            <p class="text-gray-900 leading-none">Jonathan Reinink</p>
                        </nuxt-link>
                        <div class="mt-1 -ml-1">
                            <svg class="w-4 h-4 text-gray-500 inline -mt-1.5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"></path>
                            </svg>
                            <p class="inline text-sm text-gray-500">August 28,2022</p>
                        </div>

                    </div>
                </div>
                <media-icon />
            </div>
        </div>
        <hr class="w-8/12 my-6 m-auto">
        <div class="w-8/12 m-auto">
            <div>
                <img class="w-full h-96" src="https://greatpeopleinside.com/wp-content/uploads/2017/05/HR-GR8-technology.jpg" alt="">
                <h4 class="my-6 font-semibold text-lg">Can coffee make you a better developer?</h4>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Deleniti, sunt vitae at quisquam reprehenderit facilis mollitia itaque minima neque nam eos, laboriosam, ipsa voluptates. Quasi doloribus minus quod dolor blanditiis!
                    Maxime hic expedita quia quaerat accusantium nam dolorum nobis voluptatibus iste, illo dolor rerum consequuntur similique doloribus at. Ipsam ducimus, ipsa sapiente excepturi sed blanditiis aliquam. Ex sapiente cum nisi.
                    Fugit possimus assumenda quidem exercitationem. Fugit nisi nemo, doloribus maxime eaque, cum, consequatur quidem est excepturi blanditiis perferendis vitae possimus dolorem non dicta. Totam dolore libero odio enim, nostrum labore!
                    Quam vel qui impedit accusantium odit ducimus blanditiis doloremque dolores nam rem quaerat id ex veritatis reiciendis cupiditate, ullam, perspiciatis vero nostrum, nemo quae? Optio vitae voluptatum possimus cumque fugit.
                </p>
                <br>
                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Non rem odio, perferendis ut provident dolorem doloremque amet quibusdam architecto tempora molestiae optio. Voluptatem blanditiis iusto exercitationem illo officia, debitis neque!
                </p>
                <br>
                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Ipsam laboriosam pariatur perspiciatis, quis, enim quisquam asperiores officiis sequi voluptate magnam dolorem itaque sint odio nemo tempora, doloremque quas! Quisquam, magni?
                    Hic necessitatibus accusantium quas fugiat cumque aperiam ratione porro maxime, laborum pariatur ipsam aut saepe odio? Quae, reprehenderit provident repellendus, optio nobis numquam voluptatem praesentium quidem eligendi adipisci dicta voluptatum!
                    Quae quod ipsam totam id assumenda consequuntur, architecto numquam. Porro perferendis sapiente sed rem earum natus magnam, corrupti voluptatibus quam, id veniam amet, animi vero nostrum eos! Modi, dicta aliquid.
                    Cupiditate hic corporis sit blanditiis repudiandae dicta nihil ex earum alias incidunt nesciunt culpa, necessitatibus, similique voluptas praesentium soluta non repellat nulla! Non ipsa iure delectus at voluptatum vel aperiam.
                    Totam similique illo ipsum ea expedita assumenda delectus a quidem voluptates velit corrupti dignissimos autem quis perferendis soluta ipsam, iure aspernatur voluptatibus exercitationem rem enim vel debitis in sint! Consectetur.</p>
                <br>
                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Error nemo sapiente nam magni iusto! Nihil itaque adipisci distinctio numquam aspernatur fuga eaque exercitationem, qui tempore pariatur quae debitis, error placeat!
                    Assumenda explicabo praesentium libero soluta consectetur alias corrupti eius! Delectus, modi? Illo, nisi exercitationem? Dolores placeat dolor eum, iure animi consequuntur id, totam possimus, aspernatur vel ipsum incidunt similique fugiat!
                    Reprehenderit sint fuga debitis cumque voluptates ea optio accusamus voluptas! Quae quisquam excepturi veniam ratione, reiciendis temporibus laborum. Et, sed deserunt delectus distinctio ex ea dolor unde similique neque esse?
                    Dolores possimus deserunt eveniet aperiam neque unde asperiores dolorem voluptatum, molestias nam esse ipsa nemo. Modi nobis voluptates corrupti atque! Dignissimos facere tempora officiis aliquam ipsa ea eius placeat temporibus!
                    Tenetur, dolore. Nemo minus facilis incidunt. Eum quaerat beatae voluptatem enim ipsum labore cumque doloremque numquam ea! Iure harum numquam soluta libero? Id sint molestias earum incidunt, impedit recusandae non?</p>
                <div class="flex gap-6 justify-end">
                    <div class="cursor-pointer">
                        <svg class="w-8 h-8 mt-6" v-show="!like" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" @click="Islike">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"></path>
                        </svg>
                        <svg class="w-8 h-8 mt-6" v-show="like" fill="red" stroke="red" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" @click="Islike">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"></path>
                        </svg>
                        <p>1k</p>
                    </div>
                    <div>
                        <button @click="openComment">
                            <svg class="w-8 h-8 mt-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 10h.01M12 10h.01M16 10h.01M9 16H5a2 2 0 01-2-2V6a2 2 0 012-2h14a2 2 0 012 2v8a2 2 0 01-2 2h-5l-5 5v-5z"></path>
                            </svg>
                            <p>200</p>
                        </button>

                    </div>
                    <div>
                        <svg class="w-8 h-8 mt-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"></path>
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z"></path>
                        </svg>
                        <p>1,5K</p>
                    </div>
                </div>
                <hr class="w-full my-6 m-auto">

            </div>
        </div>
        <div v-show="commentModal">
            <comment-modal @closeComment="closeComment" />
        </div>

    </div>
</section>
</template>

<script>
import CommentModal from '~/components/commentModal.vue';
import mediaIcon from '~/components/mediaIcon.vue';
export default {
    components: {
        mediaIcon,
        CommentModal
    },
    layout: 'layout',
    data() {
        return {
            commentModal: false,
            like:false,
        }
    },
    methods: {
        openComment() {
            this.commentModal = true;
        },
        closeComment(toggle) {
            this.commentModal = toggle;
        },
        Islike(){
            this.like = !this.like;
        }
    }
}
</script>

<style>

</style>
