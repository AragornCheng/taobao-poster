<template>
    <main class="p-10">
        <el-form :model="form" label-width="120px">
            <el-form-item label="标题">
                <el-input v-model="form.title" />
            </el-form-item>
            <el-form-item label="描述">
                <el-input v-model="form.desc" type="textarea" />
            </el-form-item>
            <el-form-item>
                <el-button type="primary" @click="onSubmit">生成</el-button>
            </el-form-item>
        </el-form>
    </main>
</template>

<script setup>
import { reactive } from 'vue'

const form = reactive({
    title: '',
    desc: ''
})

const onSubmit = () => {
    console.log('submit!')
}
</script>
