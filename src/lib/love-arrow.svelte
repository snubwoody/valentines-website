<script lang='ts'>
    import { browser } from '$app/environment';
	import anime from 'animejs';
    import { onMount } from 'svelte';
	export let left: number | null = null;
	export let right: number | null = null;
	export let bottom: number | null = null;
	export let top: number | null = null;
	let loveArrow:HTMLElement;

	onMount(() => {
		animateArrow()
	})

	const animateArrow = () => {
		anime({
			targets:loveArrow,
			scale:[0,1],
			duration:200,
			delay:500,
			easing: 'spring(1, 50, 5, 15)'
		})
	}

	const style = {
		
	}

	const xAxis = left != null ? `left:${left}px` : `right:${right}px`
	const yAxis = top != null ? `top:${top}px` : `bottom:${bottom}px`

</script>

<img 
src="/love-arrow.webp" 
alt="" 
bind:this={loveArrow}
style={`${yAxis}; ${xAxis}`}
class={`w-[70px] aspect-square absolute`}>