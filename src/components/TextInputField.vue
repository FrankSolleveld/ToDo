<template>
    <form @submit.prevent="submitForm">
        <input class="w-full text-center my-2 pt-8 border-b" v-model="value" type="text" placeholder="Add your next todo right here!">
    </form>
</template>

<script>
    export default {
        name: "TextInputField",
        data() {
            return {
                value: '',
            }
        },
        methods: {
            submitForm() {
                console.log(this.value)
                this.$emit('addTodo', this.value)
                this.value = ''
            }
        }
    }
</script>

<style scoped>

</style>