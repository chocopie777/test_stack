<script setup>
import { ref } from 'vue';
const open = ref(false);

const showModal = () => {
    open.value = true;
};

const handleOk = (e) => {
    console.log(e);
    open.value = false;
};
</script>
<template>
    <a-flex gap="middle" horizontal justify="space-between" style="margin-bottom: 20px">
        <a-input v-model:value="value" placeholder="Найти по ФИО..." style="width:150px" />
        <a-button @click="showModal">Добавить</a-button>
    </a-flex>
    <a-modal v-model:open="open" title="Добавить организацию" @ok="handleOk">
        <a-input v-model:value="value" placeholder="Название" style="margin-bottom:10px"/>
        <a-input v-model:value="value" placeholder="Номер телефона" style="margin-bottom:10px"/>
        <a-input v-model:value="value" placeholder="ФИО директора" />
    </a-modal>
</template>