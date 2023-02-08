<script lang="ts">
	import background_art from '$lib/images/picture.png';
    import artwork from '$lib/stores/artwork';
    import test from '$lib/images/Aki_fan_art.png'

    $artwork = background_art;
    let arttoggle = true;
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>


<section>
    <!--<button on:click={() => artwork.update(() => {arttoggle = !arttoggle; return arttoggle ? background_art : test})}/>-->
	<h1>
		Галерея ANDYORSEN'a
	</h1>

	<h2>
        Это коллекция набросков, концепт-артов и другого нарисованного мной контента, который будет со временем пополняться. Контент на данной вкладке - уникальный, и его вы не увидите нигде, за некоторыми исключениями...
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

</style>