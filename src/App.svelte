<script lang="ts">

	//

	//components
	import Button from "./components/Button.svelte";
	import Card from "./components/Card.svelte";
	import Toggle from "./components/Toggle.svelte";
	import Experiment from "./components/Experiment.svelte";

	//
	interface user {
		name: string;
		bio: string;
	}

	let olly: user = {
		name: 'Olly',
		bio: 'Junior web dev working for myself',
	}

	let cardToggle: boolean;

</script>

<Experiment title={'Cards'}>
	<div class="cardContainer">
		<Card
			{...olly}
		/>
		<Card
			name={'Olly'}
			bio={'Junior web dev working for myself'}
		/>
		<Card
			name={'Olly'}
			bio={'Junior web dev working for myself'}
		/>
		<Card
			name={'Olly'}
			bio={''}
		/>
	</div>
</Experiment>

<Experiment title={'Counter'}>
	<div>
		<Button/>
	</div>
</Experiment>

<style>

	:global(body) {
		padding: 0;
		margin: 0;
	}

	:global(h1, h2, h3, h4, h5, h6) {
		padding: 0;
		margin: 0;
		font-weight: inherit;
		font-size: inherit;
	}

	.cardContainer {
		display: flex;
		padding: 1rem;
		flex-flow: row wrap;
	}

</style>