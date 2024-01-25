<script>
    const images =[
    { src: 'gallery/ct3.jpg' },
    { src: 'gallery/ct2.jpg' },
    { src: 'gallery/ct1.jpg' },
    { src: 'gallery/ct4.jpg' },
    { src: 'gallery/bct3.jpg' },
    { src: 'gallery/bct2.jpg' },
    { src: 'gallery/bct1.jpg' },
    { src: 'gallery/01.jpg' },
    { src: 'gallery/02.jpg' },
    { src: 'gallery/03.jpg' },
    { src: 'gallery/04.jpg' },
    { src: 'gallery/05.jpg' },
    { src: 'gallery/06.jpg' },
    { src: 'gallery/07.jpg' },
    { src: 'gallery/08.jpg' },
    { src: 'gallery/1.jpg' },
    { src: 'gallery/10.JPG' },
    { src: 'gallery/11.JPG' },
    { src: 'gallery/12.JPG' },
    { src: 'gallery/13.JPG' },
    { src: 'gallery/14.JPG' },
    { src: 'gallery/15.JPG' },
    { src: 'gallery/16.JPG' },
    { src: 'gallery/17.JPG' },
    { src: 'gallery/18.JPG' },
    { src: 'gallery/19.JPG' },
    { src: 'gallery/2.jpg' },
    { src: 'gallery/20.JPG' },
    { src: 'gallery/21.JPG' },
    { src: 'gallery/22.JPG' },
    { src: 'gallery/23.JPG' },
    { src: 'gallery/24.JPG' },
    { src: 'gallery/25.JPG' },
    { src: 'gallery/26.JPG' },
    { src: 'gallery/27.JPG' },
    { src: 'gallery/3.jpg' },
    { src: 'gallery/30.jpeg' },
    { src: 'gallery/31.jpeg' },
    { src: 'gallery/32.jpeg' },
    { src: 'gallery/33.jpeg' },
    { src: 'gallery/34.jpeg' },
    { src: 'gallery/35.jpeg' },
    { src: 'gallery/36.jpeg' },
    { src: 'gallery/37.jpeg' },
    { src: 'gallery/38.jpeg' },
    { src: 'gallery/39.jpeg' },
    { src: 'gallery/4.jpg' },
    { src: 'gallery/5.jpg' },
    { src: 'gallery/6.jpg' },
    { src: 'gallery/7.JPG' },
    { src: 'gallery/8.JPG' },
    { src: 'gallery/9.JPG' },
    { src: 'gallery/acm_cof.jpeg' }
]

  import Image from '../../lib/components/image.svelte';
</script>
<section>
    {#each images as image}
        <Image src={image.src} title={undefined} />
    {/each}
</section>

<style>
    section{
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
    }
</style>