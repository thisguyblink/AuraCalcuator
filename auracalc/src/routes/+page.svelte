<script>
    const values = [74, -101, -523, 711, 780, -163, 127, -47, -588, -600, 87, -519, -211, 150, -512, 407, 237, -125, 870, 986, 93, 198, 505, -985, -444, 395, -121, 913, 83, -990, 255, -54, -145, 793, 448, -964, 264, -167, 509, 209, 981, 775, -813, 96, 838, -622, -217, 565, -394, 132];
    let out = 'Cowabunga';
    let total = 0;
    let dialog;
    let val;
    let check = false;
    import alpha from '$lib/assets/alpha wolf.jpeg';

    function handleSubmit() {
        out = values[0];
    }
    function reset() {
        if (window.confirm('Are you sure you want to reset your input?')) {
            out = 'score has been reset(0)';
        }
    }
    async function getForm()  {
        let form = await request.formData()
        let group = form.getAll('value')
        window.confirm(group);
    }
    function showPop() {
        dialog.showModal();
    }
    function closePop() {
        dialog.close();
    }
    function share() {
        window.confirm("Results have been copied to clipboard");
    }
    
</script>

<div class = header>
    <h1>Aura Calcualator</h1>
    <h3>Take it if you dare!</h3>
    <h3>Are you a SIGMA or beta...</h3>
</div>
<div class ="questionList">
    <form class="questionForm" method="POST" action="?/submission">
        <input type="checkbox" id="q1" bind:checked={check}>
        <label for="q1">1. Rizzed up at least 1 person in the last week: {values[4]}</label>
        <br>
        <input type="checkbox" id="q2" value="1">
        <label for="q2">1. Rizzed up at least 1 person in the last week: {values[4]}</label>
        <br>
        <input type="checkbox" id="q3" value="2">
        <label for="q3">1. Rizzed up at least 1 person in the last week: {values[4]}</label>
        <br>
        <input type="checkbox" id="q4" value="3">
        <label for="q4">1. Rizzed up at least 1 person in the last week: {values[4]}</label>
        
        <br>
        <button type="button" id="submit" on:click={() => {
           handleSubmit();
           getForm();
        }}>Submit</button>
        <button type="button" id="reset" on:click={() => {
            reset();
         }}>Reset</button>
    </form>
    <p id="output">Your score is {total}</p>
    <div class = "results">
        <dialog id="dresult" bind:this={dialog}>
            <img alt="No found" src={alpha} />
            <p>YOUR AURA IS {total}</p>
            <button type="button" on:click={() => {
                closePop();
            }}>Exit</button>
             <button type="button" on:click={() => {
                 share();
                }}>Share</button>
        </dialog>
    </div>
    <button type="button" on:click={() => {
        showPop();
        }}>Results</button>
</div>
    
<style>
    .header {
        padding-top: 3rem;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
    }
    .questionList {
        padding-top: 3rem;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
    }
    #submit {
        background-color: green;
        color: blue
    }
    #output {
        border: 3px solid purple;
        height: 15rem;
        width: 15rem;
        background-color: beige;
    }

</style>

