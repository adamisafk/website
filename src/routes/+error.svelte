<script lang="ts">
	import { page } from '$app/stores';
</script>

<div
	class="relative mx-auto mt-28 mb-24 flex h-[20rem] w-[80vw] max-w-5xl flex-col items-start justify-start [perspective:1000px] md:h-[40rem] lg:w-[60vw]"
>
	<h1>{$page.status}: {$page.error?.message}</h1>
</div>
