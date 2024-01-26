<script lang='ts'>
    import { browser } from "$app/environment";
    import Button from "$lib/button.svelte";
    import LoveArrow from "$lib/love-arrow.svelte";
    import Yes from "$lib/yes.svelte";
	import No from "$lib/no.svelte"
    import { redirect } from "@sveltejs/kit";
    import anime from "animejs";
    import { onMount } from "svelte";

	let screenWidth:number;
	let screenHeight:number;
	let eclipse:HTMLElement;

	let yes:boolean | null = null;
	let no: boolean | null = null

	const animateCircle = () => {
		anime({
			target:eclipse,
			left: [0,550],
			scale:[0,1],
			duration:200,
			delay:500,
			loop:true

		})
	}

	if(browser){
		screenWidth = window.screen.width;
		screenHeight = window.screen.height;
	}

	
	//TODO animate circles
</script>

<main class='w-screen h-[100dvh] flex flex-col items-center justify-center gap-2 relative overflow-hidden '>
	<p class="text-xl font-bold font-['Tangerine',cursive] absolute top-0">14.02.2024</p>
	<div class='flex flex-col gap-1 items-center'>
		<p class='text-3xl font-bold font-["tangerine",cursive]'>Tionge Nkolola</p>
		<p class='text-3xl font-bold font-["tangerine",cursive]'>Will you be my</p>
		<div class="w-full px-10 ">
			<img src="/Valentine-2.webp" alt="" srcset="" class="w-full ">
		</div>
	</div>
	<div class='flex flex-col gap-5 w-fit px-5'>
		<Button fn={()=>{yes = true; no = null}}>Yes</Button>
		<Button fn={()=>{
			no = true; 
			yes = null
			setTimeout(()=>{no = null;},2500)
		}}>No</Button>
	</div>
	<LoveArrow left={0} top={5}/> 
	<LoveArrow left={70} top={30}/> 
	<LoveArrow left={0} top={50}/> 
	<LoveArrow right={0} top={5}/> 
	<LoveArrow right={70} top={30}/> 
	<LoveArrow right={0} top={60}/> 
	<LoveArrow right={70} bottom={30}/>
	<LoveArrow right={10} bottom={10}/>
	<LoveArrow left={5} bottom={50}/>
	<LoveArrow left={90} bottom={80}/>
	<LoveArrow left={90} bottom={5}/>
	<LoveArrow left={5} bottom={120}/>
	<img src="/eclipse.webp" alt="" srcset="" class="absolute right-[-170px] bottom-[-150px]">
	<img src="/eclipse.webp" alt="" srcset="" class="absolute left-[-170px] top-[-150px]">
	{#if yes}
		<Yes/>
	{/if}
	{#if no}
		<No/>
	{/if}
</main>