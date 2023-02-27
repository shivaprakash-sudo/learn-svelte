<script>
	let user = {
		loggedIn: true
	};

	const magicNumber = 42;
	// let userPrompt = prompt("Guess the magic number!");

	let cats = [
		{ id: 'J---aiyznGQ', name: 'Keyboard Cat' },
		{ id: 'z_AbfPXTKms', name: 'Maru' },
		{ id: 'OUtn3pvWmpg', name: 'Henri The Existential Cat' }
	];

	function toggle() {
		user.loggedIn = !user.loggedIn;
	}
</script>

{#if user.loggedIn}
	<button on:click={toggle}> Log in </button>
{:else}
	<button on:click={toggle}> Log out </button>
{/if}
<br />
<!-- {#if magicNumber === userPrompt}
<h2>Correct!</h2>
{:else if magicNumber > userPrompt}
<h2>Guess higher</h2>
{:else}
<h2>Guess lower</h2>
{/if} -->

<!-- {#each cats as cat}
<li><a href="https://www.youtube.com/watch?v={cat.id}">Cat: {cat.name}</a></li>
{/each} -->

{#each cats as { id, name }}
	<li><a href="https://www.youtube.com/watch?v={id}">Cat: {name}</a></li>
{/each}
