<template>
    <div>

        <div class="card">
            <Chart type="bar" :data="basicData" :options="basicOptions" />
        </div>

        <div class="card">
            <Chart type="bar" :data="moneyData" :options="basicOptions" />
        </div>
        
    </div>
</template>

<script>
import TabelaConsumo from './TabelaConsumo.vue';

export default {
    data() {
        return {
            basicData: {
                labels: ["Junho", "Julho", "Agosto", "Setembro", "Outubro", "Novembro", "Dezembro"],
                datasets: [
                    {
                        label: "Consumo Médio d'água",
                        backgroundColor: "#42A5F5",
                        data: [65, 59, 80, 81, 56, 55, 40]
                    },
                ]
            },
            moneyData: {
                labels: ["Junho", "Julho", "Agosto", "Setembro", "Outubro", "Novembro", "Dezembro"],
                datasets: [
                    {
                        label: "Gasto Médio em Reais",
                        backgroundColor: "#FFA726",
                        data: [5, 10, 15, 20, 25, 30, 40]
                    },
                ]
            },
            basicOptions: {
                plugins: {
                    legend: {
                        labels: {
                            color: "#495057"
                        }
                    }
                },
                scales: {
                    x: {
                        ticks: {
                            color: "#495057"
                        },
                        grid: {
                            color: "#ebedef"
                        }
                    },
                    y: {
                        ticks: {
                            color: "#495057"
                        },
                        grid: {
                            color: "#ebedef"
                        }
                    }
                }
            },
        };
    },
    components: { TabelaConsumo }
}
</script>

<style>
    .card{
        margin-top: 10px;
    }
</style>