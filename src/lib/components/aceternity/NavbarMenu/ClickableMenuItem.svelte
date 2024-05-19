<script lang="ts">
	import { Motion } from 'svelte-motion';

	const transition = {
		type: 'spring',
		mass: 0.5,
		damping: 11.5,
		stiffness: 100,
		restDelta: 0.001,
		restSpeed: 0.001
	};

	export let active: string | null;
	export let item: string;
	export let href: string;
</script>

<div
	on:mouseenter={() => (active = item)}
	on:mouseleave={() => (active = null)}
	class="relative"
	role="menu"
	tabindex="0"
>
	<Motion let:motion transition={{ duration: 0.3 }}>
		<a {href} use:motion class="cursor-pointer text-black hover:opacity-[0.9] dark:text-white">
			{item}
		</a>
	</Motion>
</div>
