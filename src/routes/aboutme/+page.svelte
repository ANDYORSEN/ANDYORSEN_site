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
		ANDYORSEN's Origins
	</h1>

	<h2>
        Всё началось 19 сентября 2014 года. В тот день, вдохновившись играми жанра мморпг я решил построить из лего небольшой городок. Из него начался лор ныне покойной игры "BrickWorld". Моим друзьям, которые приходили ко мне домой было интересно исследовать построенный мною кирпичный мир. Но в рамках нескольки килограмм лего и половины моей комнаты было тесновато, и долго это продолжаться не могло.

		21 августа 2016 года была выпущена первая версия BrickWorld на пк. В ней было мало чего, но так как у меня было много планов на эту игру, меня было уже не остановить. Игра развивалась свыше года. Я пытался перенести ту ламповую атмосферу в диджитал формат. И... Частично у меня это получилось.

		Реконструкция первой версии BrickWorld
		Старейшая сохранившаяся версия BrickWorld

		Последняя вышедшая версия BrickWorld. Была создана в 2020-м году. Примечательна обновлённым дизайном и была по сути попыткой воскрешения проекта.

		Начало лета 2017 года. Сюжетная часть игры BrickWorld отпочковалась, и стала самостоятельным проектом. Со временем этот проект поменял множество концепций и названий. На данный момент, часть концептов, персонажей и сюжетных линий ушли в другие проекты, а игра пошла по самостоятельному сюжету и пути. 3 мая 2018 года я собрал с пола весь конструктор, и закрыл "старый" BrickWorld. Как раз в то время вышло крупное обновление для ПК версии BrickWorld, казалось бы, что может пойти не так? Может...

		Первые арты и наброски к сюжету бывшего BrickWorld, тогдашнего "ExtraHumans HalfAngels"


		Это обновление оказалось последним. Сложность в разработке и мои непрофессиональные лидерские качества обернулись могилой для проекта. Плюсом, лего-человечки не могли использоваться в комерческих целях посторонним лицам. С другой стороны, у меня был второй проект, на который я возлагал большие надежды.

		4 Марта 2019 года вышла первая глава комикса того самого проекта. Тогда он назывался "Полуангелы". Он не сыскал такую популярность как BW, однако это был эксперимент, который перерос в нечто большее, в проект моей мечты. Где-то между маем и августом 2019 года я разрабатывал проект под кодовым названием Игра Легенд, это тоже должен был быть комикс, но про него я расскажу чуть позже. 2 сентября того же года выходит уже вторая глава моего "шедевра". И она... Объективно хуже второй. Но я даже не думал останавливаться. На момент публикации второй главы уже писался сценарий к четвёртой. 17 ноября, выходит... Нет, не третья глава Полуангелов, а новый комикс под названием "Турнир Легенд". Его я решил выпускать постранично, и это была ошибка... Первая глава полностью так и не вышла. Проект был запрошен до определённого момента.

		Первая и вторая глава комикса "Полуангелы" вместе с первой главой Турнира Легенд

		С 2020-го до середины 2022-го мы с моим другом пытались сделать общий игровой проект. Одним словом, ничего толкового из этого не вышло.

		Персонаж из проекта "Cosmoid". Игра в жанре "Выживание"

		Те личные проекты были не единственными, и сейчас я расскажу о других, которые даже не полностью закрыты на данный момент. Например: Проект "Кровавая смерть" Ух, жестокое название. Это должен был быть или комикс или, внезапно, книга о мужчине, который пытался найти лекарство от кровавой болезни... Или проект под названием "Звёздный путь к мечте". Комикс или анимационная короткометражка о девушке с амбициями выше звёзд. Основная идея этого проекта была отложена и позже будет использована. И напоследок - ZerixWorld, игра, которая должна была стать воскрешением BrickWorld, но под другой обёрткой. Проект был закрыт по причине моего полного выгорания к нему.

		Что я делаю сейчас?
		Так как я разобрал все свои прошлые проекты на кучку концептов и идей, это дало мне больше пространства для экспериментов. Да и в общем я переосмыслил подход к работе над своими проектами. Например, сейчас я работаю над ремейком комикса "Турнир Легенд". Подробнее вы можете узнать о них на этом сайте во вкладке "Проекты".

		На данный момент я учусь в Киевском университете технологий и дизайна на инженера программного обеспечения (программист).В свободное время я играю в различные компьютерные игры, рисую в диджитал или в традиционном формате а также занимаюсь разработкой игр и написанием электронной музыки. Не знаю, куда меня всё это приведёт, но надеюсь я достигну много чего! И если вы прочитали аж до сюда, то я польщён тем, что ты уделил(а) время на очередного задрота с мотивацией в штанах. Хорошего дня! 
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
