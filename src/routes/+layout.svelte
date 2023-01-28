<script>
	import Header from './Header.svelte';
	import './styles.css';
</script>



<div class="app">
	<div class="gradient">
	
	</div>
	<Header />

	<main>
		<slot />
	</main>

	<footer>
		<p>© ANDYORSEN 2017-2023</p>
	</footer>
</div>

<style>
	.gradient{
		position: absolute;
		top: 0;
		left: 0;
		width: 100vw;
		height: 100%;
		background: linear-gradient(rgba(1,1,1,0), 10%,  purple);
		z-index: -1;

	}
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 12px;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>
