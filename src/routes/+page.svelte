<script>
	import Nested from './Nested.svelte';
	import Info from './Info.svelte';
	import Logic from './Logic.svelte';
	import Thing from './Thing.svelte';
	// import { apiKey } from '../config.js';
	import DomEvents from './DOMEvents.svelte';
	import InnerEvent from './InnerEvent.svelte';

	const details = {
		name: 'Shiva',
		link: 'https://linkedin.com/in/shiva-pendem'
	};

	let fruits = [
		{ id: 1, name: 'apple' },
		{ id: 2, name: 'banana' },
		{ id: 3, name: 'cherry' },
		{ id: 4, name: 'grapes' },
		{ id: 5, name: 'kiwi' },
		{ id: 6, name: 'lemon' }
	];

	function handleClick() {
		fruits = fruits.slice(1);
	}

	// async function getRandomMoviePoster() {
	// 	const randomNum = Math.floor(Math.random() * 1000000);
	// 	console.log(randomNum);
	// 	const result = await fetch(`https://www.omdbapi.com/?s=Batman&type=movie&apikey=${apiKey}}`);
	// 	const data = await result.json();
	// 	console.log(data);
	// 	return data.Search[randomNum].Poster;
	// }

	// let poster = getRandomMoviePoster();

	// function handlePosterClick() {
	// 	poster = getRandomMoviePoster();
	// }

	function handleEventClick(event) {
		alert(event.detail.music);
	}
</script>

<!-- <h3>Props</h3>
<Nested answer={42} />

<h3>Default Props</h3>
<Nested />

<h3>Object props</h3>

<Info name={details.name} link={details.link} />

<h3>Spread props</h3>

<Info {...details} />

<Logic />
<br />

<div>
	<button on:click={handleClick}> Remove first fruit </button>

	{#each fruits as fruit (fruit.id)}
		<Thing name={fruit.name} />
	{/each}
</div>

<div>
	{#await poster}
		<p>Loading...</p>
	{:then url}
		<button on:click={handlePosterClick}>Get random poster</button>
		<img class="poster" src={url} alt="Movie poster" />
	{:catch error}
		<p class="error">Something went wrong! {error.message}</p>
	{/await}
</div> -->

<!-- <DomEvents /> -->

<InnerEvent on:message={handleEventClick} />

<!-- <style>
	.poster {
		width: 13rem;
		max-width: 100%;
		border-radius: 0.5rem;
	}
	.error {
		color: red;
	}
</style> -->
