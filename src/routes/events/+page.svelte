<script lang="ts">
	import { formatDate } from '$lib/utils'
	import * as config from '$lib/config'

	export let data
	const colors = ['#E1F8DC', '#ACDDDE', '#FFE7C7', '#FFE7C7' ];

  // Function to get a random color from the array
  function getRandomColor() {
    const randomIndex = Math.floor(Math.random() * colors.length);
    return colors[randomIndex];
  }
</script>

<svelte:head>
	<title>{config.title}</title>
</svelte:head>

<section>
	<h3>Events</h3>
	<ul class="posts">
		{#each data.posts as post}
		<a href={post.slug}>
		<div class="container" style="background-color: {getRandomColor()};">
			<li class="post" style={"padding:20px"}>
				<div class="title" style="color:black">{post.title}</div>
				<p class="date">{formatDate(post.date)}</p>
				<p class="description">
				{post.description}
				</p>
			</li>
		</div>
	</a>
			
		{/each}
	</ul>
</section>

<style>
	.posts {
		display: flex;
		flex-direction: row;
		flex-wrap: wrap;
		gap: var(--size-4);
		justify-content: space-between;
		justify-content:flex-start;
		align-items: flex-start;
		padding: 2%;
	}
	a{
		text-decoration: none;
		transition: transform 0.3s ease-in-out;
	}
	a:hover{
		background-color: rgba(0,0,0,0.2);
		transform: scale(1.05);
	}
	.container{
		border-radius: 10px;
		box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
		height: 250px;
		width: 350px;
		overflow: hidden;
		padding: 2%;
	}
	.post {
		max-inline-size: var(--size-content-4);
	}
	p{
		font-size: 15px;
	}
	.post:not(:last-child) {
		border-bottom: 1px solid var(--border);
		padding-bottom: var(--size-7);
	}

	.title {
		font-size: var(--font-size-fluid-1);
		text-transform: capitalize;
	}

	.date {
		color: var(--text-2);
	}

	.description {
		color: var(--text-3);
	}

</style>
