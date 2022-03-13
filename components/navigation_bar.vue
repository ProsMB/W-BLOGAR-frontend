<template>
<section>
    <div class="fixed overflow-hidden z-[111]" v-show="nav">
        <div class="h-screen w-80 bg-white z-[111] fixed top-0 left-0 m-auto" v-show="menuLeft">
            <div>
                <div class="flex justify-between p-6">
                    <nuxt-link to="/home">
                        <div class="flex items-center justify-center flex-shrink-0 text-black mr-6">
                            <svg class="w-9 h-9 mr-2 text-blue-800 rounded shadow-lg shadow-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 20H5a2 2 0 01-2-2V6a2 2 0 012-2h10a2 2 0 012 2v1m2 13a2 2 0 01-2-2V7m2 13a2 2 0 002-2V9a2 2 0 00-2-2h-2m-4-3H9M7 16h6M7 8h6v4H7V8z"></path>
                            </svg>
                            <span class="font-semibold text-xl tracking-tight hover:hover:text-blue-800 pt-4">W-BLOGAR</span>
                        </div>
                    </nuxt-link>

                    <button class="border rounded text-black hover:border-black hover:text-white hover:bg-gray-300" @click="showMenu">
                        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <title>Close Menu</title>
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
                        </svg>
                    </button>
                </div>
                <hr>
                <div class="flex items-center w-auto">
                    <div class="text-sm flex-grow">
                        <nuxt-link to="/home" class="my-4 block ml-6 text-black hover:text-blue-800 mr-4 uppercase font-semibold">
                            BLOG
                        </nuxt-link>
                        <hr>
                        <!-- <nuxt-link to="#" class="my-4 block ml-6 text-black hover:text-blue-800 mr-4 uppercase font-semibold">
                            COMMUNITY
                        </nuxt-link>
                        <hr> -->
                        <nuxt-link to="/explore" class="my-4 block ml-6 text-black hover:text-blue-800 mr-4 uppercase font-semibold">
                            EXPLORE
                        </nuxt-link>
                        <hr>
                        <nuxt-link to="/profile/profile" class="my-4 block ml-6 text-black hover:text-blue-800 uppercase font-semibold">
                            PROFILE
                        </nuxt-link>
                        <hr>
                        <div class="flex my-4 items-start justify-center w-auto ">
                            <img class="w-20 h-20 rounded-full inline cursor-pointer" @click="showlogoutLeft" src="https://alrigh.com/wp-content/uploads/2020/06/10-Midoriya-Izuku-profile-picture-1024x1018.jpg" alt="">
                        </div>
                        <div class="w-full h-full grid grid-rows-4 justify-center -mt-4" v-show="logoutLeft">
                            <div class="inline-flex mt-2 space-y-4 pl-4">
                                <svg class="w-4 h-4 mt-5 text-gray-500 hover:text-black" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z"></path>
                                </svg>
                                <p class="text-sm">: Jonathan Reinink</p>
                            </div>
                            <div class="inline-flex -mt-2 space-y-4 pl-4">
                                <svg class="w-4 h-4 mt-5 text-gray-500 hover:text-black" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path>
                                </svg>
                                <p class="text-sm">: jonathan.reinink@gmail.com</p>
                            </div>
                            <div class="inline-flex -mt-6 space-y-4 pl-4">
                                <svg class="w-4 h-4 mt-5 text-gray-500 hover:text-black" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                    <path d="M12 14l9-5-9-5-9 5 9 5z"></path>
                                    <path d="M12 14l6.16-3.422a12.083 12.083 0 01.665 6.479A11.952 11.952 0 0012 20.055a11.952 11.952 0 00-6.824-2.998 12.078 12.078 0 01.665-6.479L12 14z"></path>
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 14l9-5-9-5-9 5 9 5zm0 0l6.16-3.422a12.083 12.083 0 01.665 6.479A11.952 11.952 0 0012 20.055a11.952 11.952 0 00-6.824-2.998 12.078 12.078 0 01.665-6.479L12 14zm-4 6v-7.5l4-2.222"></path>
                                </svg>
                                <p class="text-sm">: Software Engineer</p>
                            </div>
                            <button class="bg-gray-200 text-lg" @click="showLogout">Log out</button>
                        </div>
                        <hr>
                    </div>
                </div>
            </div>
        </div>
        <div class="h-screen w-80 bg-white z-[111] fixed  top-0 right-0 m-auto" v-show="logoutTop">
            <div>
                <div class="flex justify-between p-6">
                    <button class="border rounded text-black hover:border-black hover:text-white hover:bg-gray-300" @click="showlogoutTop">
                        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <title>Close Menu</title>
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
                        </svg>
                    </button>
                    <nuxt-link to="/home">

                        <div class="flex items-center justify-center flex-shrink-0 text-black mr-12">
                            <svg class="w-9 h-9 mr-2 text-blue-800 rounded shadow-lg shadow-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 20H5a2 2 0 01-2-2V6a2 2 0 012-2h10a2 2 0 012 2v1m2 13a2 2 0 01-2-2V7m2 13a2 2 0 002-2V9a2 2 0 00-2-2h-2m-4-3H9M7 16h6M7 8h6v4H7V8z"></path>
                            </svg>
                            <span class="font-semibold text-xl tracking-tight hover:hover:text-blue-800 pt-4">W-BLOGAR</span>
                        </div>
                    </nuxt-link>

                </div>
                <hr>
                <div class="flex items-center w-auto">
                    <div class="text-sm flex-grow">
                        <div class="flex my-4 items-start justify-center w-auto ">
                            <img class="w-20 h-20 rounded-full inline cursor-pointer" src="https://alrigh.com/wp-content/uploads/2020/06/10-Midoriya-Izuku-profile-picture-1024x1018.jpg" alt="">
                        </div>

                        <div class="w-full h-full grid grid-rows-4 justify-center -mt-4">
                            <div class="inline-flex mt-2 space-y-4 pl-4">
                                <svg class="w-4 h-4 mt-5 text-gray-500 hover:text-black" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z"></path>
                                </svg>
                                <p class="text-sm">: Jonathan Reinink</p>
                            </div>
                            <div class="inline-flex -mt-2 space-y-4 pl-4">
                                <svg class="w-4 h-4 mt-5 text-gray-500 hover:text-black" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path>
                                </svg>
                                <p class="text-sm">: jonathan.reinink@gmail.com</p>
                            </div>
                            <div class="inline-flex -mt-6 space-y-4 pl-4">
                                <svg class="w-4 h-4 mt-5 text-gray-500 hover:text-black" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                    <path d="M12 14l9-5-9-5-9 5 9 5z"></path>
                                    <path d="M12 14l6.16-3.422a12.083 12.083 0 01.665 6.479A11.952 11.952 0 0012 20.055a11.952 11.952 0 00-6.824-2.998 12.078 12.078 0 01.665-6.479L12 14z"></path>
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 14l9-5-9-5-9 5 9 5zm0 0l6.16-3.422a12.083 12.083 0 01.665 6.479A11.952 11.952 0 0012 20.055a11.952 11.952 0 00-6.824-2.998 12.078 12.078 0 01.665-6.479L12 14zm-4 6v-7.5l4-2.222"></path>
                                </svg>
                                <p class="text-sm">: Software Engineer</p>
                            </div>
                            <button class="bg-gray-200 text-lg" @click="showLogout">Log out</button>
                        </div>
                        <hr>
                    </div>
                </div>
            </div>
        </div>
        <div class="h-full w-full bg-gray-900 opacity-50 z-40 fixed top-0 scrollbar-hide left-0 m-auto"></div>
    </div>
    <nav class="flex items-center justify-between flex-wrap bg-white py-6 md:px-24 px-12 shadow-gray shadow-lg z-40">
        <nuxt-link to="/home">

            <div class="flex items-center flex-shrink-0 text-black mr-6">
                <svg class="w-9 h-9 mr-2 text-blue-800 rounded shadow-lg shadow-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 20H5a2 2 0 01-2-2V6a2 2 0 012-2h10a2 2 0 012 2v1m2 13a2 2 0 01-2-2V7m2 13a2 2 0 002-2V9a2 2 0 00-2-2h-2m-4-3H9M7 16h6M7 8h6v4H7V8z"></path>
                </svg>
                <span class="font-semibold text-xl tracking-tight hover:text-blue-800 pt-4">W-BLOGAR</span>
            </div>
        </nuxt-link>

        <div class="block md:hidden">
            <button class="flex items-center px-3 py-2 border rounded text-black border-black hover:text-white hover:bg-gray-300" @click="showMenu">
                <svg class="fill-current h-4 w-4" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                    <title>Menu</title>
                    <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
                </svg>
            </button>
        </div>
        <div class="w-full hidden md:flex md:items-center md:w-auto">
            <div class="text-sm md:flex-grow">
                <nuxt-link to="/home" class="block mt-4 md:inline-block md:mt-0 text-black hover:text-blue-800 mr-4 uppercase font-semibold link-underline link-underline-black">
                    BLOG
                </nuxt-link>
                <!-- <nuxt-link to="#" class="block mt-4 md:inline-block md:mt-0 text-black hover:text-blue-800 mr-4 uppercase font-semibold link-underline link-underline-black">
                    COMMUNITY
                </nuxt-link> -->
                <nuxt-link to="/explore" class="block mt-4 md:inline-block md:mt-0 text-black hover:text-blue-800 mr-4 uppercase font-semibold link-underline link-underline-black">
                    EXPLORE
                </nuxt-link>
                <nuxt-link to="/profile/profile" class="block mt-4 md:inline-block md:mt-0 text-black hover:text-blue-800 mr-4 uppercase font-semibold link-underline link-underline-black">
                    PROFILE
                </nuxt-link>
                <div class="pt-4 items-start w-auto inline cursor-pointer" @click="showlogoutTop">
                    <img class="w-12 h-12 rounded-full inline" src="https://alrigh.com/wp-content/uploads/2020/06/10-Midoriya-Izuku-profile-picture-1024x1018.jpg" alt="">
                </div>
            </div>
        </div>
    </nav>
    <confirm-logout v-show="logout" @closeDialog="closeDialog" @logouted="logouted" />

</section>
</template>

<script>
import confirmLogout from '~/components/confirmLogout.vue';
export default {
    components:{confirmLogout},
    data() {
        return {
            nav: false,
            menuLeft: false,
            logoutLeft: false,
            logoutTop: false,
            logout:false,
        }
    },
    methods: {
        showMenu() {
            this.nav = !this.nav;
            this.menuLeft = !this.menuLeft;
            this.logoutLeft = false;
        },
        showlogoutTop() {
            this.logoutTop = !this.logoutTop;
            this.nav = this.logoutTop;

        },
        showlogoutLeft() {
            this.logoutLeft = !this.logoutLeft;
        },
        
        showLogout(){
            this.logout = true;
        },
        closeDialog(toggle){
            this.logout = toggle;
        },
        logouted(toggle){
            this.logout = toggle;
            this.$router.push('/login');
        }
    },
    mounted() {

    }

}
</script>

<style>

</style>
