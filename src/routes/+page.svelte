<script lang='ts'>
    import { browser } from "$app/environment";
    import Button from "$lib/button.svelte";
    import LoveArrow from "$lib/love-arrow.svelte";
    import { redirect } from "@sveltejs/kit";
    import anime from "animejs";
    import { onMount } from "svelte";

	let screenWidth:number;
	let screenHeight:number;
	let eclipse:HTMLElement;

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
		screenWidth > 600 ? redirect(308,'/not_permitted') : null;
		console.log(screenWidth)
	}

	onMount(()=>{animateCircle()})
	let items = [0,1,2,3]

	
	//TODO animate circles
</script>

<main class='w-screen h-screen flex flex-col items-center justify-center gap-2 relative overflow-hidden '>
	<p class="text-xl font-bold font-['Tangerine',cursive] absolute top-0">14.02.2024</p>
	<div class='flex flex-col gap-1 items-center'>
		<p class='text-3xl font-bold font-["tangerine",cursive]'>Tionge Nkolola</p>
		<p class='text-3xl font-bold font-["tangerine",cursive]'>Will you be my</p>
		<div class="w-full px-10 ">
			<img src="/Valentine-2.png" alt="" srcset="" class="w-full ">
		</div>
	</div>
	<div class='flex flex-col gap-5'>
		<Button fn={()=>{redirect(308,'/yes')}}>Yes</Button>
		<Button fn={()=>{}}>No</Button>
	</div>
	<LoveArrow left={0} top={5}/> 
	<LoveArrow left={70} top={30}/> 
	<LoveArrow left={0} top={50}/> 
	<LoveArrow left={screenWidth-70} top={10}/> 
	<LoveArrow left={screenWidth-70} top={60}/>
	<LoveArrow left={screenWidth-70} top={110}/> 
	<div class="absolute flex items-center justify-between bottom-0 left-0 h-fit w-screen">
		{#each items as item}
			<img src="/love-arrow.png" alt=""  class={`w-[70px] aspect-square`}>
		{/each}
	</div> 

	<img src="/eclipse.png" alt="" srcset="" class="absolute right-[-170px] bottom-[-150px]">
	<img src="/eclipse.png" alt="" srcset="" class="absolute left-[-170px] top-[-150px]">
</main>