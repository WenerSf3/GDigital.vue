<template>
    <div id="app">
        <h2>Redirects</h2>
        <div class="container">
            <b-table small :fields="fields" :items="items" responsive="sm">
                <!-- A virtual column -->
                <template #cell(index)="data">
                    {{ data.index + 1 }}
                </template>

                <!-- A custom formatted column -->
                <template #cell(name)="data">
                    <b class="text-info">{{ data.value.last.toUpperCase() }}</b>, <b>{{ data.value.first }}</b>
                </template>

                <!-- A virtual composite column -->
                <template #cell(nameage)="data">
                    {{ data.item.name.first }} is {{ data.item.age }} years old
                </template>

                <!-- Optional default data cell scoped slot -->
                <template #cell()="data">
                    <i>{{ data.value }}</i>
                </template>
            </b-table>
        </div>
        <br>
        <h2>Links</h2>
        <div class="container">
            <b-table small :fields="fields" :items="items" responsive="sm">
                <!-- A virtual column -->
                <template #cell(index)="data">
                    {{ data.index + 1 }}
                </template>

                <!-- A custom formatted column -->
                <template #cell(name)="data">
                    <b class="text-info">{{ data.value.last.toUpperCase() }}</b>, <b>{{ data.value.first }}</b>
                </template>

                <!-- A virtual composite column -->
                <template #cell(nameage)="data">
                    {{ data.item.name.first }} is {{ data.item.age }} years old
                </template>

                <!-- Optional default data cell scoped slot -->
                <template #cell()="data">
                    <i>{{ data.value }}</i>
                </template>
            </b-table>
        </div>
    </div>
</template>
  
<script>

export default {
    data: function () {
        return {
            fields: [

                { key: 'nome_link', label: 'nome_link' },
                { key: 'link_hash', label: 'link_hash' },
                { key: 'max_click', label: 'max_click' },
                { key: 'created_at', label: 'created_at' }
            ],

            items: [
                { name: { first: 'John', last: 'Doe' }, sex: 'Male', age: 42 },
            ],
            }
        }

    }


</script>