<script>
    import { createEventDispatcher } from 'svelte';

    export let game;

    const emitEvent = createEventDispatcher();

    const deleteGame = (id) => {
        emitEvent('delete-game', id);
    };
</script>

<main>
    <div class="game-item">
        <img src={game.image_url} alt="Game image" class="game-img" />

        <div class="game-content">
            <h4>{game.name}</h4>

            <p>
                Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                Excepturi dolorem vel, quia ad dicta natus.
            </p>
        </div>

        <div on:click={() => deleteGame(game.id)} class="close-btn">x</div>
    </div>
</main>

<style lang="scss" scoped>
    .game-item {
        @apply relative bg-gray-200 my-4 rounded-xl flex 
            flex-col overflow-hidden h-full;

        img {
            @apply w-full h-full;
        }

        .game-img {
            @apply w-full h-48 object-cover object-center
                lg:h-64;
        }

        .game-content {
            @apply p-4 lg:text-left;

            h4 {
                @apply font-bold text-lg lg:border-l-4 lg:border-red-400 pl-4;
            }
        }

        .close-btn {
            @apply absolute h-8 w-8 flex items-center justify-center left-3 top-3 z-10
                bg-gray-200 text-red-600 rounded-full font-black cursor-pointer
                hover:bg-gray-50 hover:shadow-lg;
        }
    }
</style>
