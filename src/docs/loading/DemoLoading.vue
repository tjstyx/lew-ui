<script setup lang="ts">
import { DemoLoading1, DemoLoading1_code } from './demo';

const columns = [
    {
        title: '参数名',
        width: '200px',
        field: 'param',
    },
    {
        title: '描述',
        width: '320px',
        field: 'description',
    },
    {
        title: '类型',
        width: 'auto',
        field: 'type',
    },
    {
        title: '默认值',
        width: '200px',
        field: 'default',
    },
];
const docsTable = ref([
    {
        param: 'isShow',
        description: '是否展示',
        type: 'boolean',
        default: 'false',
    },
    {
        param: 'title',
        description: '加载文字提示',
        type: `string`,
        default: '""',
    },
]);
</script>
<template>
    <div class="demo-wrapper">
        <lew-title>Loading</lew-title>
        <lew-demo-box title="普通" :code="DemoLoading1_code">
            <demo-loading1 />
        </lew-demo-box>
        <lew-title size="16px">Props</lew-title>
        <lew-table :data="docsTable" :columns="columns" height="auto">
            <template #param="{ row }"> {{ row.param }} </template>
            <template #description="{ row }"> {{ row.description }} </template>
            <template #type="{ row }"> {{ row.type }} </template>
            <template #default="{ row }"> {{ row.default }} </template>
        </lew-table>
    </div>
</template>
