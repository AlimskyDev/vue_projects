<template>
    <div>
        <ul>
            <li v-for="(item, index) in todos" @click="deleteItem(index)" :key="index">{{ item }}</li>
        </ul>
    </div>
</template>

<script>
    export default {
        props: ['todos'],
        methods: {
            deleteItem(index){
                this.$emit('delete-item', index);
            }
        }
    }
</script>

<style>
    
</style>