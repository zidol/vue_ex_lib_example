<template>
    <canvas id="lineChart" ref="lineChart" width="400" height="400"></canvas>
</template>

<script>
export default {
    mounted() {
        const labels = [
            'January',
            'February',
            'March',
            'April',
            'May',
            'June',
        ];
        const data = {
            labels: labels,
            datasets: [{
                label: 'My First dataset',
                backgroundColor: 'rgb(255, 99, 132)',
                borderColor: 'rgb(255, 99, 132)',
                data: [0, 10, 5, 2, 20, 30, 45],
            }]
        };
        
        const config = {
            type: 'line',
            data,
            options: {}
        };
        var lineChart = new this.$_Chart(
            // document.getElementById('lineChart'),
            this.$refs.lineChart,
            config,
        );
        console.log(lineChart)
    },
}
</script>

<style>

</style>