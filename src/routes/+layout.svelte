<script lang="ts">
	import Header from './Header.svelte'
	import './styles.css'

    // let variable_name: variable_type = variable_value
    let paralax_offset: String = "0px"

    // можеш поменять переменную чтоби изменить скорость паралакса
    let paralax_ratio: number = 1

    function paralax() {
        // здесь ми находим насколько прокручена страница
        // || означаєт ИЛИ тоесть если window.scrollY не существуєт ми берем window.scrollTop
        // || здесь используєтся потому что в разних браузерах в разних местах хранится прокрутка такчто || позволяєт коду работать во всех браузерах
        // про (<any>window) пока не волнуйся ето я убегаю от проги которая говорит где у меня ошибки в коде
        let scrollPos: number = window.scrollY || (<any>window).scrollTop || document.getElementsByTagName("html")[0].scrollTop;

        // здесь px прибавляєтся в конце потому что calc  не работаєт с еденицами без розмерок
        paralax_offset = scrollPos * paralax_ratio + "px"
    }
</script>

<!-- здесь ми заставляєм код ждать пока страница не будет крутится і когда она крутится ми виполняєм функцию paralax-->
<svelte:window on:scroll={paralax}/>

<div class="app">
    <!-- все что в {} ето JS код. Такчто можно взять переменную і вставить в HTML -->
	<div style="--offset: {paralax_offset}" class="gradient"/>
	<Header />

	<main>
		<slot />
	</main>

	<footer>
		<p>© ANDYORSEN 2017-2023</p>
	</footer>
</div>

<style>
	.gradient {
		position: absolute;
		top: 0;
		left: 0;
		width: 100vw;
		height: 100%;
        /* здесь ми можем взять переменную которую засунули в HTML і с помощью calc посчитать паралакс */
		background: linear-gradient(rgba(1, 1, 1, 0) calc(55vh - var(--offset)), purple calc(65vh - var(--offset)));
		z-index: -1;
	}

	.app {
        position: relative;
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
