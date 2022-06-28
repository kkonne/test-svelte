<script>
    import GameItem from './GameItem.svelte';

    export let games = [];
</script>

<main>
    <div class="games-list">
        {#each games as game}
            <GameItem {game} on:delete-game />
        {/each}
    </div>
</main>

<style lang="scss" scoped>
    .games-list {
        @apply grid grid-cols-1 lg:grid-cols-3 gap-4 lg:gap-8 w-full;
    }
</style>
