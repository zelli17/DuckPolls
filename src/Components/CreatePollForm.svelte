
<script>
	import Button from "../Shared/Button.svelte";

    let fields  = {question: '', answerA: '', answerB: ''}

    const submitHandler = () =>{
        console.log(fields);
    }

</script>

<!-- svelte-ignore a11y-click-events-have-key-events -->
<form on:click|preventDefault={submitHandler}>

    <div class="form-field">    
        <label for="question">Poll Question</label>
        <input type="text" id="question" required bind:value={fields.question}>
    </div>
    <div class="form-field">
        <label for="answer-a">Poll Question A:</label>
        <input type="text" id="answer-a" required bind:value={fields.answerA}>
    </div>
    <div class="form-field">
        <label for="answer-b">Poll Question B:</label>
        <input type="text" id="answer-b" required bind:value={fields.answerB}>
    </div>
    <Button type="primary" flat={true}>
        Add poll

    </Button>  


</form>

<style>
    form{
        width: 500px;
        margin: 0 auto;
        text-align: center;
        /* border: solid rgb(58, 135, 84); */
      
        border-radius: 6px;

    }

    .form-field{
        margin: 18px auto;
    }

    label{
        margin: 10px auto;
        text-align: center;

    }

    input{
        width: 50%;
        border-radius: 6px;
    }

</style>