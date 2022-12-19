<template>
    <section
        class="intro relative flex items-center text-center m-10 mt-20 text-white z-10 md:text-left md:p-20 md:mt-0">
        <div class="flex items-center flex-col space-y-9 md:w-1/3 md:items-start ">
            <h2 class="text-4xl font-bold">Real Estate advice for real locals.</h2>
            <p>
                In expecting display, thought. Rationally and at it's of
                headline proper then met harmonies; Sign the had no
                made reached are desk mars might to first
            </p>
            <Button text="Get Started" class="w-fit" />
        </div>

    </section>
</template>

<script>
import Button from './Button.vue';

export default {
    name: 'Intro',
    components: {
        Button
    },
}

</script>
