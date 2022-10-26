<template>
    <div class="meta">

        <Knob v-model="metaDiária" valueTemplate="{value}%"/>
        <Knob v-model="metaSemanal" valueTemplate="{value}%"/>
        <Knob v-model="metaMensal" valueTemplate="{value}%" />

    </div>
</template>


<script>
export default {
    data() {
	return {
		metaDiária:20,
        metaSemanal:42,
        metaMensal:64
	}
}
}
</script>

<style scoped>
    .meta{
        display: flex;
    }
</style>