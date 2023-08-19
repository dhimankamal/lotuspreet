<script lang="ts">
	import Button from './Button.svelte';
</script>

<div class="h-screen w-screen flex items-center justify-center flex-col gap-6">
	<h1 class="text-2xl font-bold">Buttons</h1>
	<Button text="Button"  onClick={()=> console.log("Button")}/>
    <Button text="Button" loading={true}  onClick={()=> console.log("Button")} />
	<Button text="Button" disabled={true}  onClick={()=> console.log("Button")} />
	
</div>
