<script lang="ts">
	import { page } from '$app/stores';
	import logo from './twitch-logo.svg';
</script>

<header>
	<div class="corner">
		<a target='blank' href="https://twitch.tv/paperviewevents">
			<img src={logo} alt="TwitchLogo" />
		</a>
	</div>

	<nav>
		<ul>
			<li class:active={$page.path === '/'}><a sveltekit:prefetch href="/">Home</a></li>
			<li class:active={$page.path === '/about'}><a sveltekit:prefetch href="/about">About</a></li>
			<!-- <li class:active={$page.path === '/baby'}><a sveltekit:prefetch href="/baby">Meet Baby</a></li>
			<li class:active={$page.path === '/beast'}><a sveltekit:prefetch href="/beast">Meet Beast</a></li> -->
			<li class:active={$page.path === '/workout-at-home'}><a sveltekit:prefetch href="/workout-at-home">Learn about WAH</a></li>
		</ul>
	</nav>

	<div class="corner">
		<!-- TODO put something else here? github link? -->
	</div>
</header>

<style>
	header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		/* --background: rgba(255,255,255,1);
		background: var(--background); */
	}

	.corner {
		width: 3em;
		height: 3em;
	}

	.corner a {
		display: flex;
		align-items: center;
		justify-content: center;
		width: 100%;
		height: 100%;
		background-color: yellow;
	}

	.corner img {
		width: 2em;
		height: 2em;
		object-fit: contain;
	}

	nav {
		display: flex;
		justify-content: center;
		width: 100vw;
		border: 1px solid red;
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 4em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
	}

	li {
		position: relative;
		height: 100%;
	}

	li.active::before {
		--size: 6px;
		content: '';
		width: 0;
		height: 0;
		position: absolute;
		top: 0;
		left: calc(50% - var(--size));
		border: var(--size) solid transparent;
		border-top: var(--size) solid var(--accent-color);
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 1em;
		color: var(--heading-color);
		font-weight: 700;
		font-size: 0.8rem;
		text-transform: uppercase;
		letter-spacing: 10%;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: var(--accent-color);
	}
</style>
