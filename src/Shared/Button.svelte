<script>
    export let type = 'primary';
    export let flat = false;
    export let inverse = false;
</script>

<button class={type} class:flat={flat} class:inverse={inverse}>
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
        cursor: pointer;
    }

    button:hover{
        background-color: rgb(58, 135, 84);
    }

    .primary{
        background: rgb(58, 135, 84);
        color: white;
    }
    .primary:hover{
        background: rgb(36, 96, 56);

    }

    .secondary{
        background-color: white;
        color:rgb(58, 135, 84);

    }

    .inverse{
        color: rgb(58, 135, 84)
    }
    .flat{
        box-shadow: none;
    }
</style>