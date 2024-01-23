<script lang='ts'>
    import { browser } from "$app/environment";
    import Button from "$lib/button.svelte";
    import LoveArrow from "$lib/love-arrow.svelte";
    import { redirect } from "@sveltejs/kit";

	let screenWidth:number;
	let screenHeight:number;
	if(browser){
		screenWidth = window.screen.width;
		screenHeight = window.screen.height;
		screenWidth > 600 ? redirect(308,'/not_permitted') : null;
		console.log(screenWidth)
	}
</script>

<main class='w-screen h-screen flex flex-col items-center justify-center gap-2 relative '>
	<p class="text-3xl font-bold font-['Tangerine',cursive] absolute top-0">14.02.2024</p>
	<img src="/champagne.png" alt="">
	<div class='flex flex-col gap-1 items-center'>
		<p class='text-3xl font-bold font-["tangerine",cursive]'>Tionge Nkolola</p>
		<p class='text-3xl font-bold font-["tangerine",cursive]'>Will you be my</p>
		<div class="w-full px-10 ">
			<img src="/valentine.png" alt="" srcset="" class="w-full aspect-square">
		</div>
	</div>
	<div class='flex flex-col gap-5'>
		<Button>Yes</Button>
		<Button>No</Button>
	</div>
	<LoveArrow x={0} y={5}/> 
	<LoveArrow x={70} y={30}/> 
	<LoveArrow x={0} y={50}/> 
	<LoveArrow x={screenWidth-70} y={5}/> 
	<LoveArrow x={screenWidth-70} y={100}/> 
	<LoveArrow x={0} y={screenHeight-70-5}/> 
	<LoveArrow x={0} y={screenHeight-70-70}/>
	<p class="text-3xl font-bold font-['Tangerine',cursive] absolute bottom-0">XOXO</p>
</main>