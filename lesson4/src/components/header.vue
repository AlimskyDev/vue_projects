<template lang="html">
    <div>
        <div class="header" v-for="(k, index) in kaka" @click="delk(index)" :key="index">{{k}}
        </div>
    </div>
</template>
<script>
    export default {
        props:['kaka'],
        methods:{
            delk(d){
                this.$emit('dk', d);
            }
        }
    }
</script>
<style lang="css">
.header {
    width: 100%;
    height: 35px;
    padding: 5px 10px;
    background-color: blue;
    margin-top: 10px;
    color: white;
    font-size: 30px;
}
</style>