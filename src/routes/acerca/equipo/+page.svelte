<script>
	import { equipo } from '$lib';

	const algo = (e) => {
		let description = e.target.getElementsByClassName('description')[0];
		console.log(description);

		if (description.classList.contains('hidden')) {
			description.classList.remove('hidden');
		}
	};

	const algomas = (e) => {
		let description = e.target.getElementsByClassName('description')[0];

		description.classList.add('hidden');
	};
</script>

<div class="py-20 mx-14">
	<div class="flex justify-between w-full">
		{#each equipo as integrante}
			<!-- svelte-ignore a11y-no-static-element-interactions -->
			<a class="m-2" href="https://localhost/practicas/{integrante.Name}">
				<div
				class="grid grid-cols-2 justify-center w-full gap-3 transition-all font-mono rounded-lg drop-shadow-2xl shadow-inner shadow-rose-50 bg-slate-100 p-1"
				on:mouseenter={algo}
				on:mouseleave={algomas}
			>
				<img class="w-auto" src={integrante.Image} alt={integrante.Description} />
				<div class="description hidden">
					<p class="text-base transition-all">{integrante.Description}</p>
				</div>
				<p class="font-semibold text-lg">{integrante.Name}</p>
			</div>
			</a>
		{/each}
	</div>
</div>
