<template>
    <div>

        <DataTable :value="consumo" responsiveLayout="scroll">
            <Column field="code" header="Data"></Column>
            <Column field="name" header="Consumo"></Column>
            <Column field="category" header="Gasto"></Column>
        </DataTable>
        
    </div>
</template>

<script>
    export default {
        data(){
            return{
                consumo:[
                {code:'01/10/2022',name:' 30 Litros',category:'R$ 20.00'},
                {code:'02/10/2022',name:' 8 Litros',category:'R$ 11.00'},
                {code:'03/10/2022',name:' 12 Litros',category:'R$ 14.00'},
                {code:'04/10/2022',name:' 23 Litros',category:'R$ 18.00'},
                {code:'05/10/2022',name:' 14 Litros',category:'R$ 16.00'}
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