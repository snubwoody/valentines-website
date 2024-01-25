<script lang="ts">
	export let imgSrc:string;
	export let width:number = 0;
	export let aspect:string = '1/1';

	const imgWidth = `w-[${width ?? 0}px]`
	const imgAspect = `aspect-[${aspect}]`
</script>

<div class="w-fit h-fit shadow-lg bg-white border-b-[30px] border-[10px] border-white">
	<img src={imgSrc} alt="" width={`${width}px`}s srcset="" class={``}>
</div>