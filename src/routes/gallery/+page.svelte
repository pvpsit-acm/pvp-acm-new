<script>
    const images = [
    { src: 'batch-2023-24.jpg', title: 'Image 1' },
    { src: 'batch-2023-24.jpg', title: 'Image 2' },
    { src: 'batch-2023-24.jpg', title: 'Image 1' },
    { src: 'batch-2023-24.jpg', title: 'Image 2' },
    { src: 'batch-2023-24.jpg', title: 'Image 1' },
    { src: 'batch-2023-24.jpg', title: 'Image 2' },
    { src: 'batch-2023-24.jpg', title: 'Image 1' },
    { src: 'batch-2023-24.jpg', title: 'Image 2' },
    { src: 'batch-2023-24.jpg', title: 'Image 1' },
    { src: 'batch-2023-24.jpg', title: 'Image 2' },
    { src: 'batch-2023-24.jpg', title: 'Image 1' }
    // Add more images as needed
  ];
  import Image from '../../lib/components/image.svelte';
</script>
<section>
    {#each images as image}
        <Image src={image.src} title={image.title} />
    {/each}
</section>

<style>
    section{
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
    }
</style>