<script>
	let firstName = "Blin";
	let lastName = "Kukaj";
	let color = "Blue";
	let showtext = false;
	let users = [
		{ id: "1", name: "John" },
		{ id: "2", name: "Ari" },
		{ id: "3", name: "Bennet" },
	];

	$: name = firstName + " " + lastName + color;
	const toggle = () => {
		color = color === "blue" ? "red" : "blue";
		showtext = !showtext;
		users = [...users, {id : '4', name: 'Sara'}]
	};
</script>

<h1 style="color: {color}">Hello {name}</h1>
{#if showtext}
	<p>
		Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn
		how to build Svelte apps.
	</p>
{:else}
	<p>No Text</p>
{/if}
<button on:click={toggle}>Click </button>
{#each users as user (user.id)}
	<h3>{user.name}</h3>
{/each}

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
