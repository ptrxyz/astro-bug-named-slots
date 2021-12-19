<script>
    import Button from './Button.svelte'
    // const Button = document.require('./Button.svelte')

    let count = 0

    function add() {
        count += 1
    }

    function subtract() {
        count -= 1
    }
</script>

<div class="counter">
    <button on:click={subtract}>-</button>
    <pre>{count}</pre>
    <button on:click={add}>+</button>
</div>
<div class="message">
    <slot name="msg" />
</div>
<Button>Something</Button>

<style>
    .counter {
        display: grid;
        font-size: 2em;
        grid-template-columns: repeat(3, minmax(0, 1fr));
        margin-top: 2em;
        place-items: center;
    }
    .message {
        text-align: center;
    }
</style>
