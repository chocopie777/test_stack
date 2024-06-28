<script setup>
const columns = [
    {
        title: 'Название',
        dataIndex: 'name',
        key: 'name',
        sorter: true,
    },
    {
        title: 'ФИО директора',
        dataIndex: 'fio',
        key: 'fio',
        sorter: true,
    },
    {
        title: 'Номер телефона',
        dataIndex: 'number_phone',
        key: 'number_phone',
    },
    {
        title: '',
        key: 'remove',
        dataIndex: 'remove',
    },
];
const data = [
  {
    key: '1',
    name: 'ООО "Ромашка"',
    fio: "Иванов Иван Иванович",
    number_phone: '88005552525',
    remove: '',
  },
  {
    key: '2',
    name: 'ИП Владимиров В.В"',
    fio: "Владимиров Владимир Владимирович",
    number_phone: '89424443324',
    remove: '',
  },
  {
    key: '3',
    name: 'ИП Васильев В.В"',
    fio: "Васильев Василий Васильевич",
    number_phone: '89322233212',
    remove: '',
  },
];
</script>
<template>
    <a-table :dataSource="data" :columns="columns" bordered>
        <template #bodyCell="{ column }">
            <template v-if="column.dataIndex === 'remove'">
                <a-flex justify="center">
                    <a-button type="primary" danger>X</a-button>
                </a-flex>
            </template>
        </template>
    </a-table>
</template>