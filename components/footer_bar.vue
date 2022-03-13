<template>
<section>
    <footer class="p-4 bg-gray-200 sm:p-6 dark:bg-gray-800 shadow-gray shadow-lg z-40 border-t-2">
        <div class="md:flex md:justify-between">
            <div class="mb-6 md:mb-0">
                <nuxt-link to="/" class="flex items-center">
                    <svg class="w-9 h-9 mr-2 text-blue-800 rounded shadow-lg shadow-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 20H5a2 2 0 01-2-2V6a2 2 0 012-2h10a2 2 0 012 2v1m2 13a2 2 0 01-2-2V7m2 13a2 2 0 002-2V9a2 2 0 00-2-2h-2m-4-3H9M7 16h6M7 8h6v4H7V8z"></path>
                        </svg>
                    <span class="self-center text-xl font-semibold whitespace-nowrap dark:text-white pt-4">W-BLOGAR</span>
                </nuxt-link>
            </div>
            <div class="grid grid-cols-2 gap-8 sm:gap-6 sm:grid-cols-3">
                <div>
                    <h3 class="mb-6 text-sm font-semibold text-gray-900 uppercase dark:text-white">Resources</h3>
                    <ul>
                        <li class="mb-4">
                            <a href="https://flowbite.com" target="_blank" class="text-gray-600 hover:underline dark:text-gray-400">W-BLOGAR</a>
                        </li>
                        <li>
                            <a href="https://tailwindcss.com/" target="_blank" rel="nofollow" class="text-gray-600 hover:underline dark:text-gray-400">Tailwind CSS</a>
                        </li>
                    </ul>
                </div>
                <div>
                    <h3 class="mb-6 text-sm font-semibold text-gray-900 uppercase dark:text-white">Follow us</h3>
                    <ul>
                        <li class="mb-4">
                            <a href="https://github.com/themesberg/flowbite" target="_blank" class="text-gray-600 hover:underline dark:text-gray-400">Github</a>
                        </li>
                        <li>
                            <a href="https://discord.gg/4eeurUVvTy" target="_blank" class="text-gray-600 hover:underline dark:text-gray-400">Discord</a>
                        </li>
                    </ul>
                </div>
                <div>
                    <h3 class="mb-6 text-sm font-semibold text-gray-900 uppercase dark:text-white">Legal</h3>
                    <ul>
                        <li class="mb-4">
                            <a href="#" target="_blank" class="text-gray-600 hover:underline dark:text-gray-400">Privacy Policy</a>
                        </li>
                        <li>
                            <a href="#" target="_blank" class="text-gray-600 hover:underline dark:text-gray-400">Terms &amp; Conditions</a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
        <hr class="my-6 border-gray-200 sm:mx-auto dark:border-gray-700 lg:my-8">
        <div class="sm:flex sm:items-center sm:justify-between">
            <span class="text-sm text-gray-500 sm:text-center dark:text-gray-400">© 2022 <a href="https://flowbite.com" target="_blank" class="hover:underline">W-BLOGAR</a>. All Rights Reserved.
            </span>
            <media-icon/>
        </div>
    </footer>
</section>
</template>

<script>
import MediaIcon from './mediaIcon.vue'
export default {
    components:{MediaIcon},

}
</script>

<style>

</style>
