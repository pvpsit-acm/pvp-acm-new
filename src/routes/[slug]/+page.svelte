<script lang="ts">
    import { formatDate } from '$lib/utils'

    export let data
    import Image from './image.svelte';
</script>

<svelte:head>
    <title>{data.meta.title}</title>
    <meta property="og:type" content="article" />
    <meta property="og:title" content={data.meta.title} />
</svelte:head>

<article class="container">
    <div class="description-side">
        <hgroup>
            <h1 style="text-align:left;">{data.meta.title}</h1>
            <p>Conducted on {formatDate(data.meta.date)}</p>
        </hgroup>

        <div class="tags" >
            {#each data.meta.categories as category}
                <span class="surface-4">&num;{category}</span>
            {/each}
        </div>

        <div >
            <svelte:component this={data.content} />
        </div>
    </div>

    <div class="image-side">
        <!-- Replace 'your_image_path.jpg' with the actual path to your image -->
        <!-- svelte-ignore a11y-img-redundant-alt -->
            <Image src={data.meta.image} title={data.meta.title} />
    </div>
</article>

<style>
    .container {
        display: flex;
        margin-top: 10px;
    }

    .description-side {
		max-width: 100%;
		width:100%;
        flex: 1;
        margin-right: 1px;
		text-align: justify;
       /* Adjust as needed */
    }

    .image-side {
        flex: 1;
    }

    img {
        max-width: 100%;
        height: auto;
        border: 1px solid #ccc;
    }

    h1 {
        text-transform: capitalize;
    }

    h1 + p {
        margin-top: var(--size-2);
        color: var(--text-2);
    }

    .tags {
        display: flex;
        gap: var(--size-3);
        margin-top: var(--size-7);
    }

    .tags > * {
        padding: var(--size-2) var(--size-3);
        border-radius: var(--radius-round);
    }
</style>
