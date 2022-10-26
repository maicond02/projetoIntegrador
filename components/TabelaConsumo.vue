<template>
    <div>

        <DataTable :value="consumo" responsiveLayout="scroll">
            <Column field="code" header="Diário"></Column>
            <Column field="name" header="Semanal"></Column>
            <Column field="category" header="Mensal"></Column>
        </DataTable>
        
    </div>
</template>

<script>
    export default {
        data(){
            return{
                consumo:[
                {code:'Diário',name:'Semanal',category:'Mensal'}
            ],
            }
        }
    }
</script>

<style scoped>
    div{
        margin-top: 50px;
    }
</style>