<script lang="ts" setup>
const openWithDelay = (type: string) => {
    // @ts-ignore
    LewNotification[type]({
        title: '通知',
        content: '我会自己消失哦',
        delay: 1500,
    });
};
const openWithoutDelay = (type: string) => {
    // @ts-ignore
    LewNotification[type]({
        title: '通知',
        content: '没有得到你的允许之前我是不会消失的！',
        delay: 0,
    });
};
</script>

<template>
    <lew-flex wrap x="start" gap="20px">
        <lew-button type="error" @click="openWithDelay('error')">
            WithDelay
        </lew-button>
        <lew-button type="success" @click="openWithoutDelay('success')">
            WithoutDelay
        </lew-button>
    </lew-flex>
</template>
