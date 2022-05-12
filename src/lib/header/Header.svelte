<script>
	import { page } from '$app/stores';
</script>

<header>
	<nav>
		<ul>
			<li class:active={$page.url.pathname === '/'}><a sveltekit:prefetch href="/">Home</a></li>
		</ul>
	</nav>

	<div class="corner">
	</div>
</header>

<style>
	
</style>
