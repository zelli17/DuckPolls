<script>
    export let type = 'primary';
    export let flat = false;
    export let  inverse = false;
</script>

<button class={type} class:flat={flat}>
    <slot></slot>
</button>


<style>
    
    button{
        background-color: gray;
        border-radius: 10px;
        width: 200px;
        border: 0;
        padding: 8px 12px;
        font-weight: bold;
        box-shadow: 1px 2px 3px (0,0,0,0.2);
    }

    button:hover{
        background-color: rgb(58, 135, 84);
    }

    .primary{
        background-color: rgb(58, 135, 84);
    }

    .secondary{
        background-color: rgb(58, 135, 84);

    }
</style>