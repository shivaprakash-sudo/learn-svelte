<script>
	let a = 1;
	let b = 3;
</script>

<div>
	<div>
		<input type="number" bind:value={a} min="0" max="10" /><input
			type="range"
			value={a}
			min="0"
			max="10"
		/>
	</div>
	<div>
		<input type="number" bind:value={b} min="0" max="10" /><input
			type="range"
			value={b}
			min="0"
			max="10"
		/>
	</div>
	<div>
		{a} + {b} = {a + b}
	</div>
</div>
