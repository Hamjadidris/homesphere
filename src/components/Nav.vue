<template>
    <nav class="relative flex justify-center z-20 w-full py-6">
        <div class="flex w-10/12 items-center  justify-between">
            <div class="flex space-x-20 pt-2">
                <h1 class="text-white text-3xl">Homesphere</h1>

                <div class="hidden space-x-8 items-center md:flex">
                    <a href="#" class=" text-white hover:text-blue-300">How it Works</a>
                    <a href="#" class=" text-white hover:text-blue-300">Features</a>
                    <a href="#" class=" text-white hover:text-blue-300">About</a>
                </div>
            </div>

            <Button text="Contact Us" class="hidden md:block" />

            <button id="menu-btn" @click="toggleNav" class="block hamburger md:hidden focus:outline-none"
                :class="(showNav)?'open':''">
                <span class="hamburger-top"></span>
                <span class="hamburger-middle"></span>
                <span class="hamburger-bottom"></span>
            </button>
        </div>

        <div class=" z-30" v-show="showNav">
            <div id="menu"
                class="absolute flex flex-col items-center text-xl self-end py-8 mt-16 space-y-6 font-bold sm:w-auto sm:self-center left-6 right-6 drop-shadow-md">
                <a href="#" class=" text-black  hover:text-white">How it Works</a>
                <a href="#" class=" text-black hover:text-white">Features</a>
                <a href="#" class=" text-black hover:text-white">About</a>
                <a href="#" class=" text-black hover:text-white">Contact Us</a>
            </div>
        </div>
    </nav>
</template>


<script >
import Button from './Button.vue';
export default {
    name: 'Nav',
    data() {
        return {
            showNav: false
        }
    },
    methods: {
        toggleNav() {
            this.showNav = !this.showNav
        }
    },
    components: {
        Button
    },
}

</script>

<style scoped>
#menu {
    background: rgba(255, 255, 255, 0.2);
    box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
    backdrop-filter: blur(10px);
    border: 1px solid rgba(255, 255, 255, 0.3);
}

.hamburger {
    cursor: pointer;
    width: 24px;
    height: 24px;
    transition: all 0.2s;
    position: relative;
}

.hamburger-top,
.hamburger-middle,
.hamburger-bottom {
    position: absolute;
    top: 0;
    left: 0;
    width: 24px;
    height: 2px;
    background-color: black;
    transform: rotate(0);
    transition: all 0.3s;
}

.hamburger-middle {
    transform: translateY(7px);
}

.hamburger-bottom {
    transform: translateY(14px);
}

.open {
    transform: rotate(90deg);
    transform: translateY(0px);
}

.open .hamburger-top {
    transform: rotate(45deg) translateY(6px) translate(6px);
}

.open .hamburger-middle {
    display: none;
}

.open .hamburger-bottom {
    transform: rotate(-45deg) translateY(6px) translate(-6px);
}
</style>
