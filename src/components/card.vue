<template>
    <div class="shadow-lg z-10 rounded-3xl">
        <div class="card flex bg-white rounded-3xl flex-col space-y-3 justify-end text-left pb-2 pl-5 transition ease-in-out hover:-translate-y-1 duration-300 hover:scale-110">
            <div class="flex  bg-blue-200 w-8 py-2 justify-center items-center rounded-lg ">
                <p class="text-blue-700 text-2xl">
                    {{ img }}
                </p>
            </div>
            <h2 class="text-blue-700 text-2xl font-bold"> {{ stat }} </h2>
            <p>{{ text }}</p>
        </div>
    </div>

</template>

<script>
export default {
    name: 'Card',
    props: {
        text: String,
        stat: String,
        img: String
    },
}
</script>

<style scoped>
.card {
    height: 12rem;
    width: 9rem;
    clip-path: polygon(0 0, 100% 23%, 100% 100%, 0% 100%);
}
</style>