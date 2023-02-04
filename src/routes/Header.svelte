<script>
</script>

<header>

<nav>
	<div class="left">
        <a href="/aboutme">Обо мне</a>
		<a href="">Новости</a>
	</div>
    <a class="logo" href="/">ANDYORSEN</a>
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
        transform: translateY(2px);
    }

	header {
		z-index: 5;
		position: fixed;
		display: flex;
		justify-content: space-between;
	}

	nav {
		height: 6.5vh;
		width: 100vw;
		background-color: #8646e0;
		display: flex;
		justify-content: center;
		--background: rgba(255, 255, 255, 0.7);
		font-family: RobotoBold;

	}

	nav a {
        overflow-x: hidden;
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 0.5rem;
		color: var(--color-text);
		font-weight: 700;
		font-size: 1.2rem;
		text-transform: uppercase;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: var(--color-theme-1);
	}
</style>
