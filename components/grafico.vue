<template>
    <div>

        <div class="card">
            <Chart type="bar" :data="basicData" :options="basicOptions" />
        </div>

        <div class="card">
            <Chart type="bar" :data="basicData" :options="basicOptions" />
        </div>
        
    </div>
</template>

<script>
import TabelaConsumo from './TabelaConsumo.vue';

export default {
    data() {
        return {
            basicData: {
                labels: ["January", "February", "March", "April", "May", "June", "July"],
                datasets: [
                    {
                        label: "My First dataset",
                        backgroundColor: "#42A5F5",
                        data: [65, 59, 80, 81, 56, 55, 40]
                    },
                    {
                        label: "My Second dataset",
                        backgroundColor: "#FFA726",
                        data: [28, 48, 40, 19, 86, 27, 90]
                    }
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