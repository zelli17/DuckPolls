
<script>
    let fields  = {question: '', answerA: '', answerB: ''}

    const submitHandler = () =>{
        console.log(fields);
    }

</script>

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
    <button>Add Poll</button>
    


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

    button{
        background-color: rgb(58, 135, 84);
        border-radius: 10px;
        width: 200px;
    }

    button:hover{
        background-color: white;
    }
</style>