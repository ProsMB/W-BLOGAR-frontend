<template>
  <section>
      <div class="flex items-center justify-center flex-shrink-0 text-black mr-6 pt-12">
        <svg class="w-12 h-12 mr-1 text-blue-800 rounded shadow-lg my-6 shadow-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 20H5a2 2 0 01-2-2V6a2 2 0 012-2h10a2 2 0 012 2v1m2 13a2 2 0 01-2-2V7m2 13a2 2 0 002-2V9a2 2 0 00-2-2h-2m-4-3H9M7 16h6M7 8h6v4H7V8z"></path>
        </svg>
        <span class="font-semibold text-2xl tracking-tight hover:text-blue-800 mt-12 my-6 text-shadow-md">W-BLOGAR</span>
    </div>
    <div class="flex items-center justify-center mt-8">
        <div class="w-full max-w-md">
            <form class="bg-white shadow-md rounded px-8 pt-6 pb-8 mb-4">
                <div class="mb-4 text-center">
                    <span class="font-semibold text-blue-800 text-2xl underline">Login</span>
                </div>
                <div class="mb-4">
                    <label class="block text-gray-700 text-sm font-bold mb-2" for="email">
                        Email
                        <span class="text-red-500">*</span>
                    </label>
                    <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-blue-500 focus:shadow-outline" id="email" type="text" placeholder="example@gmail.com" required>
                </div>
                <div class="mb-6">
                    <label class="block text-gray-700 text-sm font-bold mb-2" for="password">
                        Password
                        <span class="text-red-500">*</span>
                    </label>
                    <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 mb-3 leading-tight focus:outline-blue-500 focus:shadow-outline" id="password" type="password" placeholder="******************" required>
                    <p class="text-red-500 text-xs italic">Please choose a password.</p>
                </div>
                <div class="flex items-center justify-between">
                     <p class="text-sm">Don't have an account yet?<nuxt-link class="text-blue-400" to="/signup">Signup</nuxt-link></p>
                    <button class="bg-blue-600 hover:bg-blue-800 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline" type="button" @click="login">
                        Submit
                    </button>
                </div>
            </form>
            <p class="text-center text-gray-500 text-xs">
                &copy;2022 W-BLOGAR. All rights reserved.
            </p>
        </div>

    </div>
  </section>
</template>

<script>
export default {
    methods:{
        login(){
            this.$router.push('/home');
        }
    }

}
</script>

<style>

</style>