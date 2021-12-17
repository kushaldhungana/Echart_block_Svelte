<script>
	import Chart from "./Chart.svelte";
	export let name;
</script>

<div>
	<h1>This is the implementation of Echart block in {name}!</h1>
<Chart/>
</div>

<style>
	h1 {
	  color: #000000;
	  text-align: center;
	  font-size: 1.5em;
	  font-weight: 100;
	}

	div {
	  background-color: grey;
	  padding: 2%;
	  margin: 0;
	}
</style>