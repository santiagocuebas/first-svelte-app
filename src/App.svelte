<script lang="ts">
  import { onMount } from 'svelte';
	import Testimony from './components/Testimony.svelte';
	
	let testimonies = [];

	onMount(async () => {
		testimonies = await fetch('data.json')
			.then(res => res.json());
	});
</script>

<div class='App'>
  <div class='main-container'>
    <h1 class='title-testimony'>
			Here is what our alumni say about freeCodeCamp:
		</h1>
    {#each testimonies as testimony}
			<Testimony {...testimony} />
		{/each}
  </div>
</div>

<style>
	:global(html, body) {
		font-size: 18px;
		background-color: #f5f6f7;
	}

	.main-container {
		display: grid;
		justify-content: center;
		padding: 20px 0;
		gap: 60px;
	}

	.title-testimony {
		text-align: center;
		margin: 0;
		padding: 0;
	}
</style>
