<script lang="ts">
	import { formatDate } from '$lib/utils'
	import * as config from '$lib/config'
	import Quote from '../lib/components/quote.svelte'
	import ErrorMsg from '../lib/components/errormsg.svelte'
	import Image from '../lib/components/image.svelte'
</script>

<svelte:head>
	<title>{config.title}</title>
</svelte:head>

<section>
	<!-- <div class="main">
		<ErrorMsg />
	</div> -->
	<div class="title">
		<h3>Welcome to ACM Student Chapter - PVPSIT</h3>
	</div>
	<div class="tagline-container">
		<p class="tagline">Explore<span class="tagline-separator">|</span>Learn<span class="tagline-separator">|</span>Innovate</p>
	  </div>
	<div class="description">
		<p>Welcome to the official home of the ACM Student Chapter at PVP Siddhartha Institute of Technology (PVPSIT). Here, we are more than just a student organization; we are a vibrant community dedicated to fostering innovation, learning, and collaboration in the field of computing.</p>
	</div>
	<Quote quote="An investment in knowledge pays the best interest." author="Benjamin Franklin" />
	<div class="Images">
		<Image src="batch-2023-24.jpg" title="Student Members Batch 2023-24" />
	</div>
</section>

<style>
	.main {
		display: flex;
		align-items: center;
		justify-content: center;
		padding: 1%;
	}
	.Images {
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
	}
	.title {
		display: flex;
		align-items: flex-start;
		justify-content: center;
		padding: 1%;
	}
	.description {
		display: flex;
		align-items: center;
		justify-content: center;
		padding: 1%;
	}
	.tagline-container {
      text-align: center;
	  justify-content:  center;
	  display: flex;
      padding: 2px; /* Container background color */
      border-radius: 8px; /* Container border radius */ /* Box shadow for a subtle effect */
    }

    .tagline {
      font-size: 24px;
      color: #333; /* Text color */
    }

    .tagline-separator {
      color: #777; /* Separator color */
      margin: 0 10px;
    }
</style>
