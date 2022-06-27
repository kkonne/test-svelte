<script>
    import logo from './assets/svelte.png';
    import Counter from './lib/Counter.svelte';
    import Slideshow from './lib/Slideshow.svelte';
    import { gamesData, imagesData } from './assets/data/mockData';
    import GamesList from './lib/GamesList.svelte';

    const images = imagesData;
    let games = gamesData;

    const deleteGame = (event) => {
        const gameId = event.detail;

        games = games.filter((game) => {
            return game.id !== gameId;
        });
    };
</script>

<main class="app">
    <div class="text-center py-16 px-8 bg-red-200">
        <img src={logo} alt="Svelte Logo" class="mx-auto h-32" />
        <h1>Hello world!</h1>

        <Counter />

        <GamesList {games} on:delete-game={deleteGame} />
    </div>

    <Slideshow {images} />
</main>

<style>
</style>
