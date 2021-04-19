<script context="module" lang="ts">
	export const prerender = true;
</script>

<script lang="ts">
	import RecentEvent from '$lib/RecentEvent.svelte';
</script>

<svelte:head>
	<title>Welcome to Paper View Events</title>
</svelte:head>

<section>
	<div class='welcome-headers'>
		<h1>
			Paper View Events
		</h1>
		<h2>"Welcome to Prime Time"</h2>
	</div>

	<iframe width="860" height="540" src="https://www.youtube.com/embed/zuRn298rcT4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

	<div id='recent-events'>
		<h3>Recent Events</h3>
		<div class='event-list'>
			<RecentEvent
				name="Paper View Events #2: A Baby and the Beast"
				img='https://scontent-bos3-1.xx.fbcdn.net/v/t1.6435-9/174078961_10100656923382424_1281001526461726845_n.jpg?_nc_cat=111&ccb=1-3&_nc_sid=340051&_nc_ohc=kVinyae4akkAX-V4xkw&_nc_ht=scontent-bos3-1.xx&oh=6b054380f383a506c50583c1b779861f&oe=60A46695'
				link='https://www.facebook.com/events/786045325352442'
			/>
			<RecentEvent
				name="Paper View Events #1: The Beast vs. A Baby"
				img='https://scontent-bos3-1.xx.fbcdn.net/v/t1.6435-9/155064753_10100644308537674_9031313519171836170_n.jpg?_nc_cat=104&ccb=1-3&_nc_sid=340051&_nc_ohc=d9MsnYZWQUkAX_J7-xy&_nc_ht=scontent-bos3-1.xx&oh=126030ae7ca48858f057ee7adbe138b7&oe=60A3CDD2'
				link='https://www.facebook.com/events/185166972989537'
			/>
		</div>
	</div>
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		align-items: center;
		flex: 1;
		background: black;
	}

	h1 {
		width: 100%;
		font-size: 7rem;
		padding: 0;
		margin: 0;
		background: rgb(236,255,0);
		background: linear-gradient(45deg, rgba(236,255,0,1) 35%, rgba(255,0,0,1) 50%, rgba(236,255,0,1) 65%);
		background: -webkit-linear-gradient(45deg, rgba(236,255,0,1) 35%, rgba(255,0,0,1) 50%, rgba(236,255,0,1) 65%);
		background-clip: text;
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
	}

	h2 {
		font-size: 5rem;
		padding: 0;
		margin: 0;
		font-family: 'Bradley Hand';
		background: linear-gradient(135deg, rgba(236,255,0,1) 35%, rgba(255,0,0,1) 65%);
		background: -webkit-linear-gradient(135deg, rgba(236,255,0,1) 35%, rgba(255,0,0,1) 65%);
		background-clip: text;
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
	}

	#recent-events {
		width: 100%;
		text-align: left;
	}

	.event-list {
		width: 100%;
		display: flex;
		overflow-x: scroll;
	}

	h3 {
		font-size: 4rem;
		padding: 0;
		margin: 0;
		font-family: 'Bradley Hand';
		background: linear-gradient(45deg, rgba(236,255,0,1) 35%, rgba(255,0,0,1) 50%, rgba(236,255,0,1) 65%);
		background: -webkit-linear-gradient(45deg, rgba(236,255,0,1) 35%, rgba(255,0,0,1) 50%, rgba(236,255,0,1) 65%);
		background-clip: text;
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
	}

	.welcome {
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	}
</style>
