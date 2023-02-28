<script>
	let pos = {
		x: 0,
		y: 0
	};

	function handleClick(event) {
		pos.x = event.clientX;
		pos.y = event.clientY;
	}
</script>

<div>
	<h3>Mouse position</h3>
	<p>
		x: {pos.x}
		<br />
		y: {pos.y}
	</p>
	<button on:click={handleClick}>Click me</button>
</div>

<style>
	div {
		width: 100%;
		height: 100vh;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}
</style>
