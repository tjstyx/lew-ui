<template>
    <lew-flex gap="20px"
        >请看右下角
        <lew-back-top target="app-main" @click="getEvent"></lew-back-top>
        <lew-back-top right="100px" target="app-main">
            <div>UP</div>
        </lew-back-top>
    </lew-flex>
</template>
<script lang="ts" setup>
const getEvent = () => {
    console.log('回到顶部');
};
</script>
