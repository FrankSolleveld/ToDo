<template>
    <div>
        {{item.title}}
    </div>
</template>

<script>
    export default {
        name: "ListItem",
        props: {
            item: Object
        }
    }
</script>

<style scoped>

</style>