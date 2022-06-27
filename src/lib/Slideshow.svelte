<script>
    export let images = [];
</script>

<main>
    <div class="slideshow">
        <div class="left-shadow slideshow-shadow" />
        <div class="right-shadow slideshow-shadow" />

        <div class="assets">
            {#each images as image (image.id)}
                <img src={image.url} alt={image.alt_text} />
            {/each}
        </div>
        <div class="assets">
            {#each images as image (image.id)}
                <img src={image.url} alt={image.alt_text} />
            {/each}
        </div>
    </div>
</main>

<style lang="scss">
    .slideshow {
        @apply relative w-full overflow-x-hidden h-40 flex items-center justify-start bg-gray-900;
        .slideshow-shadow {
            @apply absolute z-10 top-0 w-12 h-full;
        }
        .left-shadow {
            @apply left-0 bg-gradient-to-r from-gray-200
            dark:from-gray-900;
        }
        .right-shadow {
            @apply right-0 bg-gradient-to-l from-gray-200
            dark:from-gray-900;
        }
        .assets {
            @apply flex items-center justify-start min-w-max;
            animation: slide 40s linear infinite;
            img {
                @apply h-12 mx-4 md:mx-8 2xl:mx-16;
                filter: brightness(10) grayscale(1);
            }
        }
        @keyframes slide {
            100% {
                transform: translateX(-100%);
            }
        }
    }
</style>
