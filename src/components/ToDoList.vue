<template>
    <div>
       <ListItem v-for="(item, index) in todos" :key="index" :item="item"/>
    </div>
</template>

<script>
    import ListItem from "./ListItem";
    export default {
        name: "ToDoList",
        components: {ListItem},
        props: {
            todos: Array
        }
    }
</script>

<style scoped>

</style>