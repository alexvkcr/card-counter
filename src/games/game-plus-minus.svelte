<script>
    import GameBox from "../game-box.svelte";
    import CloseGameToMenu from "../close-game-to-menu.svelte";
</script>

<style>
    :global(body.dark-mode) * {
        color: white;
    }
</style>

<GameBox>
    <CloseGameToMenu on:closeGame />
    <div>The game</div>
</GameBox>
