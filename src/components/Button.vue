<template>
    <a href="#" class="p-3 px-6  text-white rounded-full bg-blue-700 baseline hover:bg-blue-500 "> {{ text }}</a>
</template>

<script>
export default {
    name: "Button",
    props: {
        text: String,
    },
}
</script> 
