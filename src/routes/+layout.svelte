<script lang="ts">
	import Header from './Header.svelte'
    import './styles.css'
    import { onMount } from 'svelte';

    // let variable_name: variable_type = variable_value
    let scrollpos: number = 0

    onMount(async () => {
        scrollpos = window.scrollY || (<any>window).scrollTop || document.getElementsByTagName("html")[0].scrollTop
    })
    // можеш поменять переменную чтоби изменить скорость паралакса
    let paralax_ratio: number = 1

    function paralax() {
        // здесь ми находим насколько прокручена страница
        // || означаєт ИЛИ тоесть если window.scrollY не существуєт ми берем window.scrollTop
        // || здесь используєтся потому что в разних браузерах в разних местах хранится прокрутка такчто || позволяєт коду работать во всех браузерах
        // про (<any>window) пока не волнуйся ето я убегаю от проги которая говорит где у меня ошибки в коде
        scrollpos = window.scrollY || (<any>window).scrollTop || document.getElementsByTagName("html")[0].scrollTop;
    }

    import artwork from '$lib/stores/artwork';
</script>

<!-- здесь ми заставляєм код ждать пока страница не будет крутится і когда она крутится ми виполняєм функцию paralax-->
<svelte:window on:scroll={paralax}/>

<div class="app" style="--scroll: {scrollpos * paralax_ratio}px">
    <!-- все что в {} ето JS код. Такчто можно взять переменную і вставить в HTML -->
	<Header />

    <main class="gradient">
        <div class="artwork">
            <img src="{$artwork}" alt="artwork">
        </div>
        <div class="main-content">
            <slot/>
        </div>
    </main>

	<footer>
		<p>© ANDYORSEN 2017-2023</p>
	</footer>
</div>

<style>
    :global(:root) {
        --artwork-size: 70vh;
    }

    .artwork {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        z-index: -1;
        display: flex;
        justify-content: center;
        overflow-x: hidden;
    }
    .artwork img {
        height: var(--artwork-size);
    }

	.gradient {
		width: 100vw;
		height: 100%;
        /* здесь ми можем взять переменную которую засунули в HTML і с помощью calc посчитать паралакс */
		background: linear-gradient(rgba(1, 1, 1, 0) calc(var(--artwork-size) - 10vh - var(--scroll)), #6637a3 calc(var(--artwork-size) - var(--scroll)));
    }
    .main-content {
		max-width: 64rem;
		margin: 0 auto;
        padding-top: calc(var(--artwork-size) - min(var(--artwork-size) / 2, var(--scroll)));
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
		box-sizing: border-box;
        position: relative;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 12px;
		background-color: #48258f;
	}

	footer p {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>
