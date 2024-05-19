<script lang="ts">
	import { WavyBackground } from '$lib/components/aceternity';
	import { page } from '$app/stores';
	console.log($page.url.host);
</script>

<WavyBackground className="max-w-4xl mx-auto pb-40">
	<p class="inter-var text-center text-2xl font-bold text-white md:text-4xl lg:text-7xl">
		{$page.url.host}
	</p>
	<p class="inter-var mt-4 text-center text-base font-normal text-white md:text-lg">Welcome</p>
</WavyBackground>
