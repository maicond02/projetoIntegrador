<template>
    <div>

        <Card class="d-card">
            <template #title>
                Casa
            </template>
            <template #content>
               <p>Acesse seus dados de Consumo detalhado, veja o gráfico diário, semanal e mensal</p> <br>
            </template>
            <template #footer>
                <nuxt-link to="/gastos">
                    <Button icon="pi pi-reply" label="Acessar"/>
                </nuxt-link>            
            </template>
        </Card>
        
        <Card class="d-card">
            <template #title>
                Meta de Consumo
            </template>
            <template #content>
                <Meta/>
            </template>
        </Card>

    </div>
</template>

<style scoped>
a{
    text-decoration: none;
}
.d-card{
    margin-top: 10px;
}
</style>