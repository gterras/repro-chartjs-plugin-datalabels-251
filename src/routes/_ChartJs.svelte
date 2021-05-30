<script >

	// Chart.js
	import ChartJS from 'chart.js/auto/auto.js'
	
	// Chart.js datalabels plugin 
	import ChartDataLabels from 'chartjs-plugin-datalabels'
	ChartJS.register(ChartDataLabels)
	
	export let options

	const chart = (node, options) => {

		const opts = Object.assign({}, options);
		const chart = new ChartJS(node, opts)

		return {
			destroy() {
				chart.destroy()
			}

		}
	}

</script> 

<canvas use:chart={options}></canvas>

