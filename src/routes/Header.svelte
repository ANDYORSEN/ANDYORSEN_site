<script>
</script>

<header>

<nav>
	<div class="left">
		<a href="">Обо мне</a>
		<a href="">Новости</a>
	</div>
	<a class="logo" href="">ANDYORSEN</a>
	<div>
		<a href="">Проекты</a>
		<a href="">ЧаВо</a>
	</div>
</nav>

</header>

<style>
	.logo {
		font-size: 1.5em;
	}
	.left {
		justify-content: end;
	}
	div {
		flex: 1;
        overflow: hidden;
		display: flex;
		width: auto;
	}

    div a {
        transform: translateY(4px);
    }

	header {
		display: flex;
		justify-content: space-between;
	}

	nav {
		height: 5vh;
		width: 100vw;
		background-color: mediumpurple;
		display: flex;
		justify-content: center;
		--background: rgba(255, 255, 255, 0.7);
	}

	nav a {
        overflow-x: hidden;
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 0.5rem;
		color: var(--color-text);
		font-weight: 700;
		font-size: 0.8rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: var(--color-theme-1);
	}
</style>
