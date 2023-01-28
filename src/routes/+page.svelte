<script>
	import Counter from './Counter.svelte';
	import welcome from '$lib/images/picture.png';
	import welcome_fallback from '$lib/images/svelte-welcome.png';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<h1>
		<span class="welcome">
			<picture>
				
				<img src={welcome} alt="Welcome" />
			</picture>
		</span>

		Добро пожаловать!<br />Это сайт ANDYORSEN
	</h1>

	<h2>
		папапевегемабоди
	</h2>

</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1 {
		width: 100%;
	}

	.welcome {
		display: flex;
		justify-content: center;
		position: relative;
		width: 100%;
	}

	.welcome img {
		height: 60vh;
		top: 0;
		display: block;
	}
</style>
