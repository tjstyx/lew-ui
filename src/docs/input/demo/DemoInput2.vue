<template>
    <lew-form direction="y" style="width: 300px">
        <lew-form-item label="小的">
            <lew-input type="textarea" size="small" />
        </lew-form-item>
        <lew-form-item label="常规">
            <lew-input type="textarea" />
        </lew-form-item>
        <lew-form-item label="大的">
            <lew-input type="textarea" size="large" />
        </lew-form-item>
        <lew-form-item label="常规的">
            <lew-input type="textarea" />
        </lew-form-item>
        <lew-form-item label="可清空">
            <lew-input type="textarea" clearable />
        </lew-form-item>
        <lew-form-item label="展示数字">
            <lew-input type="textarea" show-count />
        </lew-form-item>
        <lew-form-item label="展示数字 + 可清空">
            <lew-input type="textarea" show-count clearable />
        </lew-form-item>
        <lew-form-item label="字数限制">
            <lew-input type="textarea" show-count :max-length="30" />
        </lew-form-item>
        <lew-form-item label="字数计算方式（中文=1，字母=0.5）">
            <lew-input
                type="textarea"
                placeholder="1个中文作为1个字符，而2个英文作为1个"
                show-count
                nice-count
                :max-length="30"
            />
        </lew-form-item>
        <lew-form-item label="可缩放的">
            <lew-input
                type="textarea"
                resize="vertical"
                show-count
                :max-length="30"
            />
        </lew-form-item>
    </lew-form>
</template>
