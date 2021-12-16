<script>
	import Chart from "./Chart.svelte";
	export let name;
</script>

<div>
	<h1>This is the implementation of Echart in {name}!</h1>
<Chart/>
</div>

<style>
	h1 {
	  color: #000000;
	  text-align: center;
	  font-size: 2em;
	  font-weight: 100;
	}
</style>