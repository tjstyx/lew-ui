<script setup lang="ts">
import {
    DemoInput1,
    DemoInput2,
    DemoInput1_code,
    DemoInput2_code,
} from './demo';

const docsTable = reactive([
    {
        desc: 'Props',
        columns: [
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
        ],
        data: [
            {
                param: 'type',
                description: '输入框类型（textarea：多行文本）',
                type: 'string',
                default: 'text',
            },
            {
                param: 'model-value (v-model)',
                description: '绑定值',
                type: 'string',
                default: "''",
            },

            {
                param: 'disabled',
                description: '禁用',
                type: 'boolean',
                default: 'false',
            },
            {
                param: 'placeholder',
                description: '默认提示',
                type: 'string',
                default: '请输入',
            },
            {
                param: 'readonly',
                description: '是否只读',
                type: 'boolean',
                default: 'false',
            },
            {
                param: 'clearable',
                description: '是否可清空',
                type: 'boolean',
                default: false,
            },
            {
                param: 'clear',
                description: '清空触发的回调方法',
                type: '(e: value) => void',
                default: '-',
            },
            {
                param: 'resize',
                description: '缩放模式（只对多行文本框生效）',
                type: 'string',
                default: 'none',
            },
        ],
    },
    {
        desc: 'Event',
        columns: [
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
        ],
        data: [
            {
                param: 'input',
                description: '输入',
                type: '() => void',
                default: 'false',
            },
            {
                param: 'change',
                description: '值变化',
                type: '() => void',
                default: 'false',
            },
            {
                param: 'blur',
                description: '失焦',
                type: '() => void',
                default: 'false',
            },
            {
                param: 'focus',
                description: '聚焦',
                type: '() => void',
                default: 'false',
            },
        ],
    },
]);
</script>

<template>
    <div class="demo-wrapper">
        <lew-title>Input</lew-title>
        <lew-demo-box title="单行文本框" :code="DemoInput1_code">
            <demo-input1 />
        </lew-demo-box>
        <lew-demo-box title="多行文本框" :code="DemoInput2_code">
            <demo-input2 />
        </lew-demo-box>
        <div v-for="(item, index) in docsTable" :key="index">
            <br />
            <br />
            <lew-title size="16px">{{ item.desc }}</lew-title>
            <lew-table :data="item.data" :columns="item.columns" height="auto">
                <template #param="{ row }"> {{ row.param }} </template>
                <template #description="{ row }">
                    {{ row.description }}
                </template>
                <template #type="{ row }"> {{ row.type }} </template>
                <template #default="{ row }"> {{ row.default }} </template>
            </lew-table>
        </div>
    </div>
</template>
