<script>
	import '../app.css';
	import logo from '$lib/svg/logo.svg';
	import escudo from "$lib/img/escudo-actualizado-2022.png"

	const desplegar_menu = (e)=>{
		let menu = document.getElementById("navbar-sticky")
		
		if(menu.classList.contains("hidden")){
			menu.classList.remove("hidden")
		}else{
			menu.classList.add("hidden")
		}
	}

</script>

<nav
	class="bg-gray-900 fixed w-full z-20 top-0 start-0 border-b border-gray-600"
>
	<div class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-4">
		<a href="/" class="flex items-center space-x-3 rtl:space-x-reverse">
			<img src={logo} class="h-10 logo-img" alt="Flowbite Logo" />
			<header>
				<span class="self-center text-2xl font-semibold whitespace-nowrap text-white"
					>RO-RO</span
				>
			</header>
		</a>
		<div class="flex md:order-1 space-x-3 md:space-x-0 rtl:space-x-reverse">
			<button on:click={desplegar_menu} type="button" class="inline-flex items-center p-2 w-10 h-10 justify-center text-sm text-gray-500 rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 text-gray-400 hover:bg-gray-700 focus:ring-gray-600" aria-controls="navbar-sticky" aria-expanded="false">
			  <span class="sr-only">Open main menu</span>
			  <svg class="w-5 h-5" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 17 14">
				  <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 1h15M1 7h15M1 13h15"/>
			  </svg>
		  </button>
		</div>
		<div
			class="items-center justify-between hidden w-full md:flex md:w-auto md:order-2"
			id="navbar-sticky"
		>
			<ul
				class="flex flex-col p-4 md:p-0 mt-4 font-medium border rounded-lg md:space-x-8 rtl:space-x-reverse md:flex-row md:mt-0 md:border-0 bg-gray-800 md:bg-gray-900 border-gray-700"
			>
				<li>
					<a
						href="/acerca/materia"
						class="block py-2 px-3  rounded  md:p-0 md:hover:text-blue-500 text-white hover:bg-gray-700 hover:text-white md:hover:bg-transparent border-gray-700"
						aria-current="page">Acerca de la materia</a
					>
				</li>
				<li>
					<a
						href="/acerca/equipo"
						class="block py-2 px-3 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:hover:text-blue-700 md:p-0 md:hover:text-blue-500 text-white hover:bg-gray-700 hover:text-white md:hover:bg-transparent border-gray-700"
						>Acerca del equipo</a
					>
				</li>
				<li>
					<a
						href="/actividades"
						class="block py-2 px-3 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:hover:text-blue-700 md:p-0 md:hover:text-blue-500 text-white hover:bg-gray-700 hover:text-white md:hover:bg-transparent border-gray-700"
						>Actividades</a
					>
				</li>
				<li>
					<a
						href="/acerca/pagina"
						class="block py-2 px-3 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:hover:text-blue-700 md:p-0 md:hover:text-blue-500 text-white hover:bg-gray-700 hover:text-white md:hover:bg-transparent border-gray-700"
						>Tecnologias usadas</a
					>
				</li>
			</ul>
		</div>
	</div>
</nav>

<div class="bg-gray-200"><slot /></div>

<footer class="bg-slate-800 p-5">
	<div class="grid grid-cols-1 md:grid-cols-4 gap-5">
		<div class="flex justify-center">
			
		<img src="{escudo}" class="w-52" alt="Escudo de la Universidad Autonoma de Baja California">
		</div>
		<div></div>
		<div></div>
		<div class="flex-col-reverse text-gray-400  h-full p-5">
			<div class="mb-auto"><h4 class="font-bold">Trabajo Creado para la materia:</h4>
			<ul class="list-disc list-inside">
				<li>Administración de Sistemas Operativos </li>
			</ul></div>
			<br>
			<br>
			<br>
			<br>
			<br>
			<br>
			<h4 class="mt-auto font-bold">Trabajo creado para la Universidad Autonoma de Baja Califonia.</h4>
		</div>
	</div>
</footer>

<style>
	.logo-img {
		/* to black */
		filter: invert(1);
	}

	#navbar-sticky{
		transition-delay: 0.5s;
		transition: 1s ease all;
	}
</style>
