<script>
	export let name = 'None';
	export let url = 'None';
	export let dest = '';
</script>

<div class="w-full flex justify-center bg-green-100 shadow-md shadow-cyan-900 p-5 rounded-lg">
	<a href={dest}>
		<div class="flex-col">
			<img src={url} alt={url} class="w-52 h-52 hover:scale-110 cursor-pointer transition-all" />
			<p class="text-center text-lg font-semibold mt-10">{name}</p>
		</div>
    </a>
</div>
