<template lang="">
    <div>
        <div class="items" v-for="(item, index) in shop" @click="deleteItem(index)" :key="index">
            {{item}}
        </div>
    </div>
</template>

<script>
    export default {
        props: ['shop'],
        methods: {
            deleteItem(i) {
                this.$emit('delete-item', i);
            }
        }
    }
</script>

<style lang="css">
    .items {
        display: inline;
        margin: 0 10px;
        font-size: 50px;
        border: 5px solid black;
        
    }
</style>