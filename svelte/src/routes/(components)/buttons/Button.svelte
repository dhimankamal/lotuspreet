<script lang="ts">
	export let text: string;
	export let loading: boolean = false;
	export let disabled: boolean = false;
	export let onClick: () => void;
</script>

<button
	{disabled}
	class="disabled:opacity-50 disabled:cursor-not-allowed group border rounded-md py-2 px-8 bg-blue-700 hover:bg-blue-800 flex items-center text-white gap-2 transition-all relative"
	on:click={onClick}
    class:cursor-not-allowed={loading}
>
	<div
		class="flex gap-3 py-2 items-center absolute justify-center w-full left-0 opacity-0 transition-opacity duration-100"
		class:opacity-100={loading}
	>
		<div class="w-2 h-2 rounded-full border-2 border-white bg-white" />
		<div class="w-3 h-3 rounded-full border-2 border-white animate-bounce" />
		<div class="w-2 h-2 rounded-full border-2 border-white bg-white" />
	</div>

	<div
		class="flex gap-3 py-2 items-center opacity-0 transition-opacity duration-100"
		class:opacity-100={!loading}
	>
		{text}
		<div class="w-3 h-3 rounded-full border-2 border-white" />
	</div>
</button>
