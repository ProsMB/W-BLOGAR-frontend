<template>
<section>
    <div class="h-full w-full opacity-50 bg-gray-900 z-[60] fixed top-0 left-0 m-auto"></div>
    <div class="bg-white lg:h-4/6 lg:w-4/12 z-[111] fixed top-40 md:left-[34%] left-4 p-3 m-auto rounded-xl">
         <div class="w-full flex justify-end cursor-pointer">
                    <svg class="w-7 h-7 transform hover:scale-95 duration-300 z-[80]" @click="close" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 14l2-2m0 0l2-2m-2 2l-2-2m2 2l2 2m7-2a9 9 0 11-18 0 9 9 0 0118 0z"></path>
                    </svg>
                </div>
        <form class="bg-white rounded lg:px-8 lg:pb-8 mb-4">
            <div class="mb-4 text-center">
                <span class="font-semibold text-blue-800 text-2xl underline">New Blog</span>
            </div>
            
            <div class="mb-3 grid grid-cols-2 gap-2">
                <div>
                    <label class="block text-gray-700 text-sm font-bold mb-2" for="title">
                        Title
                        <span class="text-red-500">*</span>
                    </label>
                    <input class="shadow appearance-none border rounded w-full py-1.5 px-3 text-gray-700 leading-tight focus:outline-blue-500 focus:shadow-outline" id="title" type="text" placeholder="Type here..." required>
                </div>
                <div>
                    <label class="block text-gray-700 text-sm font-bold mb-2" for="gender">
                        Category
                        <span class="text-red-500">*</span>
                    </label>
                    <div class="relative">
                        <select class="shadow block appearance-none w-full bg-white border border-gray-200 py-1.5  rounded leading-tight fo focus:bg-white focus:outline-blue-500 focus:shadow-outline" id="grid-state" required>
                            <option disabled>None</option>
                            <option>Technology</option>
                            <option>Food</option>
                            <option>Travel</option>
                            <option>Life Style</option>
                            <option>Sharing</option>
                        </select>
                        <div class="pointer-events-none absolute inset-y-0 right-0 flex items-center px-2 text-gray-700">
                            <svg class="fill-current h-4 w-4" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20">
                                <path d="M9.293 12.95l.707.707L15.657 8l-1.414-1.414L10 10.828 5.757 6.586 4.343 8z" /></svg>
                        </div>
                    </div>
                </div>
            </div>
            <div class="mb-3 grid grid-cols-2 gap-2">
                <div>
                    <label class="block text-gray-700 text-sm font-bold mb-2" for="content1">
                        Content 1
                        <span class="text-red-500">*</span>
                    </label>
                    <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-blue-500 focus:shadow-outline" id="content1" type="text" placeholder="Type here..." required>
                    <!-- <p class="text-red-500 text-xs italic">Please choose a password.</p> -->
                </div>
                <div>
                    <label class="block text-gray-700 text-sm font-bold mb-2" for="content2">
                        Content 2
                        <span class="text-red-500">*</span>
                    </label>
                    <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-blue-500 focus:shadow-outline" id="content2" type="text" placeholder="Type here..." required>
                    <!-- <p class="text-red-500 text-xs italic">Please choose a password.</p> -->
                </div>
            </div>
            <div class="mb-3 grid grid-cols-2 gap-2">
                <div>
                    <label class="block text-gray-700 text-sm font-bold mb-2" for="content3">
                        Content 3
                        <span class="text-red-500">*</span>
                    </label>
                    <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-blue-500 focus:shadow-outline" id="content3" type="text" placeholder="Type here..." required>
                </div>
                <div>
                    <label class="block text-gray-700 text-sm font-bold mb-2" for="content4">
                        Content 4
                        <span class="text-red-500">*</span>
                    </label>
                    <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-blue-500 focus:shadow-outline" id="content4" type="tel" placeholder="Type here..." required>
                </div>

            </div>
             <div class="mb-3">
                    <label class="block text-gray-700 text-sm font-bold mb-2" for="password">
                        choose image
                        <span class="text-red-500">*</span>
                    </label>
                    <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-blue-500 focus:shadow-outline" id="imageBlog" type="file" placeholder="" required>
            </div>
            <div class="flex items-center justify-end">
                <button class="bg-blue-600 hover:bg-blue-800 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline" type="submit" @click="create">
                    Create
                </button>
            </div>
        </form>
    </div>
</section>
</template>

<script>
export default {
    emits:['closeForm','createBLog'],
    methods:{
        close(){
            this.$emit('closeForm',false);
        },
        create(){
            this.$emit('createBlog',false);
        }
    }

}
</script>

<style>

</style>
