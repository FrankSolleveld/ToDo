<template>
    <div class="py-4 my-1 text-center w-full border" :class="isCompleted ? 'bg-gray-200 line-through' : 'bg-white' " @click="isCompleted =! isCompleted">
        {{item.name}} {{isCompleted}}
    </div>
</template>

<script>
    export default {
        name: "ListItem",
        props: {
            item: Object
        },
        data() {
            return {
                isCompleted: false,
            }
        }
    }
</script>

<style scoped>

</style>