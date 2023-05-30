<template lang="">
    <div>
        <div class="mat" >
            {{waiting}}
        </div>
    </div>
</template>
<script>

export default {
    props: ['waiting']
}
</script>

<style lang="css">
.mat {
    font-size: 30px;
    color: purple;
}
</style>