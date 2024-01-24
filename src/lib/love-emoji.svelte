<script lang='ts'>
    import { browser } from '$app/environment';
	import anime from 'animejs';
    import { onMount } from 'svelte';
	export let left = 0;
	export let top = 0;
	export let bottom = 0;
	export let right = 0;
	let loveArrow:HTMLElement;

	onMount(() => {
		animateArrow()
	})

	const animateArrow = () => {
		anime({
			targets:loveArrow,
			scale:[0.5,1.5,0.5,1.5],
			duration:900,
			loop:true,
			easing: 'spring(1, 80, 90, 10)'
		})
	}
</script>

<p
bind:this={loveArrow}
style={`
left: ${left}px; 
top: ${top}px;
bottom: ${bottom}px;
right: ${right}px;
`
}
class={`text-2xl`}>😍</p>