<script lang="ts">
	import '../app.css';
	import {
		NavbarMenu,
		HoveredLink,
		MenuItem,
		ProductItem,
		ClickableMenuItem
	} from '$lib/components/aceternity';

	let active: string | null = null;
</script>

<svelte:head>
	<title>The Website.</title>
</svelte:head>

<body class="dark">
	<div class="relative flex w-full items-center justify-center">
		<div class={'fixed inset-x-0 top-0 z-50 mx-auto max-w-2xl'}>
			<NavbarMenu>
				<ClickableMenuItem {active} item="Home" href="/" />
				<MenuItem {active} item="About Me">
					<div class="flex flex-col space-y-4 text-sm">
						<HoveredLink href="/about/background">Background</HoveredLink>
						<HoveredLink href="/about/whatdo">What I Do</HoveredLink>
					</div>
				</MenuItem>
				<MenuItem {active} item="Portfolio">
					<div class=" grid grid-cols-2 gap-10 p-4 text-sm">
						<ProductItem
							title="This website"
							href="/blog/1"
							src="https://images.pexels.com/photos/1031659/pexels-photo-1031659.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2"
							description="Embracing React alternatives"
						/>
					</div>
				</MenuItem>
				<ClickableMenuItem {active} item="Blog" href="/blog">
					<div class="flex flex-col space-y-4 text-sm">
						<HoveredLink href="#">Latest</HoveredLink>
						<HoveredLink href="#">Archive</HoveredLink>
					</div>
				</ClickableMenuItem>
				<MenuItem {active} item="Links">
					<div class="flex flex-col space-y-4 text-sm">
						<HoveredLink href="#">GitHub</HoveredLink>
						<HoveredLink href="#">Mastodon</HoveredLink>
						<HoveredLink href="#">Matrix</HoveredLink>
						<HoveredLink href="#">Discord</HoveredLink>
					</div>
				</MenuItem>
			</NavbarMenu>
		</div>
	</div>

	<slot />
</body>
