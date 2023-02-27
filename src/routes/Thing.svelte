<script>
	import { onDestroy } from 'svelte';

	const emojis = {
		apple: '🍎',
		banana: '🍌',
		cherry: '🍒',
		grapes: '🍇',
		kiwi: '🥝',
		lemon: '🍋'
	};

	export let name;

	const emoji = emojis[name];

	onDestroy(() => {
		console.log('destroyed item: ', name);
	});
</script>

<p>The emoji for {name} is {emoji}</p>
