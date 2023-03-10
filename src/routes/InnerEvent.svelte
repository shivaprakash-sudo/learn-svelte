<script>
	import { createEventDispatcher } from 'svelte';

	const dispatch = createEventDispatcher();

	function handleClick() {
		dispatch('message', {
			text: 'Hello from InnerEvent!',
			music: 'Playing music'
		});
	}
</script>

<button on:click={handleClick}> Click to see magic! </button>
