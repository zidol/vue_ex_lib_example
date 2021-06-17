<template>
  <canvas id="barChart" ref="barChart" width="400" height="400"></canvas>
</template>

<script>

export default {
    props : ['propsdata'],
    mounted() {
        // var ctx = document.getElementById('barChart');
        var ctx = this.$refs.barChart;
        var barChart = new this.$_Chart(ctx, {
            type: 'bar',
            data: {
                labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
                datasets: this.propsdata
            },
            options: {
                scales: {
                    y: {
                        beginAtZero: true
                    }
                }
            }
        });
        console.log(barChart)
    },
}
</script>

<style>

</style>