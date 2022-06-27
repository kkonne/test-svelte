<script>
    import logo from './assets/svelte.png';
    import Counter from './lib/Counter.svelte';
    import Slideshow from './lib/Slideshow.svelte';

    const images = [
        {
            id: 0,
            url: 'https://soling.md/images/stories/virtuemart/manufacturer/resized/cerva.png',
            alt_text: 'Brand logo image',
        },
        {
            id: 1,
            url: 'https://www.promocadeaux.com/wp-content/uploads/2020/01/kariban.png',
            alt_text: 'Brand logo image',
        },
        {
            id: 2,
            url: 'https://www.europeancatalog.eu/media/aitmanufacturers/threehundred/gildan.png',
            alt_text: 'Brand logo image',
        },
        {
            id: 3,
            url: 'https://www.bbfsafety.co.za/wp-content/uploads/2020/02/lemaitre-logo-white.png',
            alt_text: 'Brand logo image',
        },
        {
            id: 4,
            url: 'https://img2.storyblok.com/360x158/filters:quality(100)/f/68186/374x164/7a363b0390/kl-stack-logo-white.png',
            alt_text: 'Brand logo image',
        },
        {
            id: 5,
            url: 'https://sportland.com/media/wysiwyg/brandsHistoryBlockLogo/helly-hansen.png',
            alt_text: 'Brand logo image',
        },
        {
            id: 6,
            url: 'https://b2bit.ba/wp-content/uploads/2019/10/miviko-logo.png',
            alt_text: 'Brand logo image',
        },
    ];
</script>

<main class="app">
    <img src={logo} alt="Svelte Logo" />
    <h1>Hello world!</h1>

    <Counter />

    <Slideshow {images} />
</main>

<style>
</style>
