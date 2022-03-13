<template>
<section>
    <div class="flex items-center justify-center flex-shrink-0 text-black mr-6 pt-6">
        <svg class="w-12 h-12 mr-1 text-blue-800 rounded shadow-lg my-6 shadow-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 20H5a2 2 0 01-2-2V6a2 2 0 012-2h10a2 2 0 012 2v1m2 13a2 2 0 01-2-2V7m2 13a2 2 0 002-2V9a2 2 0 00-2-2h-2m-4-3H9M7 16h6M7 8h6v4H7V8z"></path>
        </svg>
        <span class="font-semibold text-2xl tracking-tight hover:text-blue-800 mt-12 my-6 text-shadow-md">W-BLOGAR</span>
    </div>

    <div class="flex items-center justify-center mt-4">
        <div class="w-full max-w-lg">
            <form class="bg-white shadow-md rounded px-8 pt-6 pb-8 mb-4">
                <div class="mb-4 text-center">
                    <span class="font-semibold text-blue-800 text-2xl underline">Signup</span>
                </div>
                <div class="mb-3 grid grid-cols-2 gap-2">
                    <div>
                        <label class="block text-gray-700 text-sm font-bold mb-2" for="firstName">
                            First Name
                            <span class="text-red-500">*</span>
                        </label>
                        <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-blue-500 focus:shadow-outline" id="firstName" type="text" placeholder="First Name" required>
                        <!-- <p class="text-red-500 text-xs italic">Please choose a password.</p> -->
                    </div>
                    <div>
                        <label class="block text-gray-700 text-sm font-bold mb-2" for="lastName">
                            Last Name
                            <span class="text-red-500">*</span>
                        </label>
                        <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-blue-500 focus:shadow-outline" id="lastName" type="text" placeholder="Last Name" required>
                        <!-- <p class="text-red-500 text-xs italic">Please choose a password.</p> -->
                    </div>
                </div>
                <div class="mb-3 grid grid-cols-2 gap-2">
                    <div>
                        <label class="block text-gray-700 text-sm font-bold mb-2" for="email">
                            Email
                            <span class="text-red-500">*</span>
                        </label>
                        <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-blue-500 focus:shadow-outline" id="email" type="text" placeholder="example@gmail.com" required>
                    </div>
                    <div>
                        <label class="block text-gray-700 text-sm font-bold mb-2" for="phone">
                            Phone
                            <span class="text-red-500">*</span>
                        </label>
                        <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-blue-500 focus:shadow-outline" id="phone" type="tel" placeholder="XXX-XXX-XXX" required>
                    </div>

                </div>
                <div class="mb-3 grid grid-cols-2 gap-2">
                    <div>
                        <label class="block text-gray-700 text-sm font-bold mb-2" for="title">
                            Title
                            <span class="text-red-500">*</span>
                        </label>
                        <input class="shadow appearance-none border rounded w-full py-1.5 px-3 text-gray-700 leading-tight focus:outline-blue-500 focus:shadow-outline" id="title" type="text" placeholder="Doctor" required>
                    </div>
                    <div>
                        <label class="block text-gray-700 text-sm font-bold mb-2" for="gender">
                            Gender
                            <span class="text-red-500">*</span>
                        </label>
                        <div class="relative">
                            <select class="shadow block appearance-none w-full bg-white border border-gray-200 py-1.5  rounded leading-tight fo focus:bg-white focus:outline-blue-500 focus:shadow-outline" id="grid-state" required>
                                <option disabled>None</option>
                                <option>Female</option>
                                <option>Male</option>
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
                        <label class="block text-gray-700 text-sm font-bold mb-2" for="password">
                            Password
                            <span class="text-red-500">*</span>
                        </label>
                        <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-blue-500 focus:shadow-outline" id="password" type="password" placeholder="******************" required>
                        <!-- <p class="text-red-500 text-xs italic">Please choose a password.</p> -->
                    </div>
                    <div>
                        <label class="block text-gray-700 text-sm font-bold mb-2" for="ConPassword">
                            Confirm Password
                            <span class="text-red-500">*</span>
                        </label>
                        <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-blue-500 focus:shadow-outline" id="conPassword" type="password" placeholder="******************" required>
                        <!-- <p class="text-red-500 text-xs italic">Please choose a password.</p> -->
                    </div>
                </div>
                <div class="flex items-center justify-between">
                    <p class="text-sm">Already have an account?<nuxt-link class="text-blue-400" to="/login">Login</nuxt-link></p>
                    <button class="bg-blue-600 hover:bg-blue-800 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline" type="submit" @click="signup">
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
        signup(){
            this.$router.push('/home');
        }
    }

}
</script>

<style>

</style>
