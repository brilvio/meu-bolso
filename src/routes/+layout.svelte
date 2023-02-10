<script>
	import '@skeletonlabs/skeleton/styles/all.css';
	import '@skeletonlabs/skeleton/themes/theme-skeleton.css';

	import { AppBar, AppShell, LightSwitch } from '@skeletonlabs/skeleton';
	import '../app.css';
	import SideBar from './components/core/SideBar.svelte';

	const year = new Date().getFullYear();
</script>

<AppShell>
	<svelte:fragment slot="header">
		<AppBar class="">
			<svelte:fragment slot="lead"><h3 class="font-semibold"><a href="/">Meu Bolso</a></h3></svelte:fragment>
			<svelte:fragment slot="trail"><LightSwitch /></svelte:fragment>
		</AppBar>
	</svelte:fragment>
	<svelte:fragment slot="sidebarLeft">
		<SideBar />
	</svelte:fragment>
	<!-- Router Slot -->
	<slot />
	<!-- ---- / ---- -->
	<svelte:fragment slot="footer">
		<div class="ml-2 flex gap-2">
			<p>Copyright © {year} brilvio</p>
			<a href="https://github.com/brilvio">https://github.com/brilvio</a>
		</div>
	</svelte:fragment>
</AppShell>
