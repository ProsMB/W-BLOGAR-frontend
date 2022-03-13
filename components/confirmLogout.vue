<template>
<section>
    <div class="h-full w-full opacity-50 bg-gray-900 z-[60] fixed top-0 left-0 m-auto"></div>
    <div class="bg-white lg:h-1/6 lg:w-3/12 z-[111] fixed top-1/3 md:left-[39%] left-20 p-3 m-auto rounded-xl text-center">
        <div class="w-full h-1/2 border-b-2 text-center text-xl">
            <p>Are you sure you want to logout?</p>
        </div>
        <div class="h-1/2 flex items-center justify-around w-11/12 m-auto text-lg">
            <button class="text-red-500 font-semibold" @click="close">
                No
            </button>
            <button class="text-blue-500 font-semibold" @click="logout">
                Yes
            </button>
        </div>
    </div>
</section>
</template>

<script>
export default {
    emits: ['closeDialog', 'logouted'],
    methods: {
        close() {
            this.$emit('closeDialog', false);
        },
        logout() {
            this.$emit('logouted', false);
        }
    }

}
</script>

<style>

</style>
