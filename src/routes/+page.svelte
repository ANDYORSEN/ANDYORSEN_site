<script lang="ts">
	import background_art from '$lib/images/artwork2.png';
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
		Добро пожаловать!<br />Это сайт ANDYORSEN
	</h1>

	<h2>
        Здесь вы можете ознакомится с моим творчеством и моими проектами. Комиксы, игры, арты и новости о всём этом.
	</h2>

	<img src="src/lib/images/picture.png">

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
