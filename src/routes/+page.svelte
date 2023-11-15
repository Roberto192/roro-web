<script>
	import rorro from '$lib/img/rorro-pirrorro.png';
	import logo from '$lib/svg/logo.svg';
	import { Img } from 'flowbite-svelte';
	import { browser } from '$app/environment';

	if (browser) {
		setTimeout(() => {
			console.log('Cargando');
			let image = document.getElementById('rorro');
			image.classList.remove('blur-sm');
		}, 1000);
	}
</script>

<div class="grid grid-cols-1 md:grid-cols-2 gap-10 px-5 py-20">
	<div class="rounded-2xl bg-slate-800 text-gray-100 shadow-lg shadow-black">
		<div class="rounded-t-2xl flex justify-center bg-slate-900 p-3">
			<h3 class=" text-4xl lg:text-7xl font-bold">¿Por qué roro?</h3>
		</div>
		<div class="p-3 text-justify lg:text-2xl">
			<p>
				Para la elección del nombre se tomo las iniciales de los integrantes para realizar el nombre
				del equipo llamado como roro, pero no del rorro pirrorro del show de caricaturas Johnny
				Test.
			</p>
		</div>
	</div>
	<!-- svelte-ignore a11y-no-static-element-interactions -->
	<div class="flex justify-center">
		<Img
			id="rorro"
			src={rorro}
			size="max-w-lg"
			alt="My gallery"
			class="rounded-lg transition-all duration-300 blur-sm w-full"
		/>
	</div>
	<!-- svelte-ignore a11y-no-static-element-interactions -->
	<div class="flex justify-center">
		<Img id="logo" src={logo} size="max-w-lg" alt="My gallery" class="w-full rounded-full" />
	</div>
	<div class="rounded-2xl bg-slate-800 text-gray-100 shadow-lg shadow-black">
		<div class="rounded-t-2xl flex justify-center bg-slate-900 p-3">
			<h3 class=" text-4xl lg:text-7xl font-bold">Equipo 6</h3>
		</div>
		<div class="p-3 text-justify lg:text-2xl flex-col m-2">
			<p class="my-5">
				Como parte del equipo 6 somos un equipo comprometido, y con dedicacion al aprender y
				demostrar nuestras habilidades fuera y dentro de clases para siempre dar lo mejor.
			</p>
			<p class="my-5">
				Nuestro logo quiere entender que somo parte del area de la tecnologia y como futuros
				ingenieros en Ingenieria en Software y Tecnologias Emergentes de la UABC.
			</p>
		</div>
	</div>
</div>
