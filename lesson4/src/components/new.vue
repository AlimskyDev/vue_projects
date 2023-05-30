<template lang="">
    <div>
        <div class="sss" v-for="(puh, index) in vata" @click="delet(index)" :key="index">{{ puh }}</div>
    </div>
</template>

<script>
export default {
    props: ['vata'],
    methods:{
        delet(i){
            this.$emit('del', i);
        }
    }
}
</script>

    <style lang="css">
        .sss {
            width: 100px;
            height: 100px;
            background-color: red;
            font-size: 70px;
            display: inline;
            margin: 0 10px;
    }
</style>