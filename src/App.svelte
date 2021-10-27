<script lang="ts">
	let counter: number = 0;

	const modifyCounter = (value: number): number => (counter += value);
	const reset = (): number => (counter = 0);
</script>

<main>
	<h1>Counter App</h1>
	<hr>
	<h2>Counter: {counter}</h2>
	<button class="add" on:click="{() => modifyCounter(1)}">Click</button>
	<button class="dim" on:click="{() => modifyCounter(-1)}">Dim</button>
	<button class="reset" on:click="{reset}">Reset</button>
</main>

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

	h2 {
		font-size: 2rem;	
	}

	button {
		padding: 0.5em;
		border: none;
		border-radius: 5px;
		color: #fff;
		font-size: 1.2em;
		font-weight: 100;
		cursor: pointer;
	}

	.add {
		background: #26d231;
	}

	.add:active {
		background: #19b623;
	}

	.dim {
		background: #3a9aea;
	}

	.dim:active {
		background: blue;
	}

	.reset {
		background: tomato;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>