<script>
    export let specialCard = undefined;
    export let milesCard = undefined
    export let stateCard = undefined;
    export let position = undefined;

</script>

<div class="player-board">
    <div id="miles-card-position" class="player-board__miles">
        {#if milesCard}
        <div class="card" id={position}>
            {#if milesCard?.img}
            <img src={milesCard?.img} alt="image of">
            {/if}
        </div>
        {/if}
    </div>
    <div id="special-card-position" class="player-board__special">
        {#if specialCard}
        <div class="card" id={position}>
            {#if specialCard[0]?.img}
            <img src={specialCard[0]?.img} alt="image of">
            {/if}
        </div>
        {/if}
    </div>
    <div id="bonus-card-position" class="player-board__bonus">
        {#if stateCard}
        <div class="card" id={position}>
            {#if stateCard?.img}
            <img src={stateCard?.img} alt="image of">
            {/if}
        </div>
        {/if}
    </div>

    <!-- <h2 class="card__title">{card.name}</h2> -->
</div>

<style>
    .player-board {
        border: solid rgb(200, 168, 121) 1px;
        width: 100%;
        height: 50%;
        display: flex;
        gap: 10px;
        justify-content: space-around;
    }
    .card{
       height: 10vh;
        padding: 2px;
        border-radius: 2px;
        background-color:transparent;
        cursor: pointer;
        transition: all 0.3s;
        z-index: 1000;
    }
    .card:hover {
        transform: translateY(-85px) scale(2.5);
        transition: all 0.3s;
        transform-origin: top ;
        z-index: 1000;
    }
    #top {
        rotate: 180deg;

    }
    #right {
        rotate: 90deg;

    }
    #left{
    rotate: -90deg;

    }
    
</style>