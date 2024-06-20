<script>
    const values = [74, -101, -523, 711, 780, -163, 127, -47, -588, -600, 87, -519, -211, 150, -512, 407, 237, -125, 870, 986, 93, 198, 505, -985, -444, 395, -121, 913, 83, -990, 255, -54, -145, 793, 448, -964, 264, -167, 509, 209, 981, 775, -813, 96, 838, -622, -217, 565, -394, 132];
    let out = 'Cowabunga';
    let total = 0;
    let dialog;
    let val;
    let checks = [false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false];
    import alpha from '$lib/assets/alpha wolf.jpeg';
    import beta from '$lib/assets/beta wolf.gif'

    function handleSubmit() {
        out = values[0];
        for (let i = 0; i < checks.length; i +=1) {
            if (checks[i]) {
                total += values[i];
            }
        }
        console.log(checks);
        console.log(total);
    }
    function reset() {
        if (window.confirm('Are you sure you want to reset your input?')) {
            out = 'score has been reset(0)';
            for (let i = 0; i < checks.length; i +=1) {
                checks[i] = false;
            }
        }
        location.reload();
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
        <!-- <input type="checkbox" id="q1" on:change={() => check[0] = !check[0]}>
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
         -->
         <input type="checkbox" id="q0" on:change={() => checks[0] = !checks[0]}>
         <label for="q0">1. Have you ever traveled outside your country?</label>
         <br>
         <input type="checkbox" id="q1" on:change={() => checks[1] = !checks[1]} checked={checks[1]}>
         <label for="q1">2. Do you prefer coffee or tea?</label>
         <br>
         <input type="checkbox" id="q2" on:change={() => checks[2] = !checks[2]} checked={checks[2]}>
         <label for="q2">3. Do you enjoy reading books?</label>
         <br>
         <input type="checkbox" id="q3" on:change={() => checks[3] = !checks[3]} checked={checks[3]}>
         <label for="q3">4. Have you ever attended a concert?</label>
         <br>
         <input type="checkbox" id="q4" on:change={() => checks[4] = !checks[4]} checked={checks[4]}>
         <label for="q4">5. Do you have any pets?</label>
         <br>
         <input type="checkbox" id="q5" on:change={() => checks[5] = !checks[5]} checked={checks[5]}>
         <label for="q5">6. Do you like to cook?</label>
         <br>
         <input type="checkbox" id="q6" on:change={() => checks[6] = !checks[6]} checked={checks[6]}>
         <label for="q6">7. Have you ever gone camping?</label>
         <br>
         <input type="checkbox" id="q7" on:change={() => checks[7] = !checks[7]} checked={checks[7]}>
         <label for="q7">8. Do you play any musical instruments?</label>
         <br>
         <input type="checkbox" id="q8" on:change={() => checks[8] = !checks[8]} checked={checks[8]}>
         <label for="q8">9. Have you ever tried skydiving?</label>
         <br>
         <input type="checkbox" id="q9" on:change={() => checks[9] = !checks[9]} checked={checks[9]}>
         <label for="q9">10. Do you enjoy watching movies?</label>
         <br>
         <input type="checkbox" id="q10" on:change={() => checks[10] = !checks[10]} checked={checks[10]}>
         <label for="q10">11. Have you ever run a marathon?</label>
         <br>
         <input type="checkbox" id="q11" on:change={() => checks[11] = !checks[11]} checked={checks[11]}>
         <label for="q11">12. Do you speak more than one language?</label>
         <br>
         <input type="checkbox" id="q12" on:change={() => checks[12] = !checks[12]} checked={checks[12]}>
         <label for="q12">13. Do you prefer cats or dogs?</label>
         <br>
         <input type="checkbox" id="q13" on:change={() => checks[13] = !checks[13]} checked={checks[13]}>
         <label for="q13">14. Have you ever been to a beach?</label>
         <br>
         <input type="checkbox" id="q14" on:change={() => checks[14] = !checks[14]} checked={checks[14]}>
         <label for="q14">15. Do you enjoy playing video games?</label>
         <br>
         <input type="checkbox" id="q15" on:change={() => checks[15] = !checks[15]} checked={checks[15]}>
         <label for="q15">16. Have you ever volunteered for a charity?</label>
         <br>
         <input type="checkbox" id="q16" on:change={() => checks[16] = !checks[16]} checked={checks[16]}>
         <label for="q16">17. Do you like spicy food?</label>
         <br>
         <input type="checkbox" id="q17" on:change={() => checks[17] = !checks[17]} checked={checks[17]}>
         <label for="q17">18. Have you ever been to a theme park?</label>
         <br>
         <input type="checkbox" id="q18" on:change={() => checks[18] = !checks[18]} checked={checks[18]}>
         <label for="q18">19. Do you enjoy gardening?</label>
         <br>
         <input type="checkbox" id="q19" on:change={() => checks[19] = !checks[19]} checked={checks[19]}>
         <label for="q19">20. Have you ever gone skiing or snowboarding?</label>
         <br>
         <input type="checkbox" id="q20" on:change={() => checks[20] = !checks[20]} checked={checks[20]}>
         <label for="q20">21. Do you like to draw or paint?</label>
         <br>
         <input type="checkbox" id="q21" on:change={() => checks[21] = !checks[21]} checked={checks[21]}>
         <label for="q21">22. Have you ever attended a sports event?</label>
         <br>
         <input type="checkbox" id="q22" on:change={() => checks[22] = !checks[22]} checked={checks[22]}>
         <label for="q22">23. Do you enjoy hiking?</label>
         <br>
         <input type="checkbox" id="q23" on:change={() => checks[23] = !checks[23]} checked={checks[23]}>
         <label for="q23">24. Have you ever tried sushi?</label>
         <br>
         <input type="checkbox" id="q24" on:change={() => checks[24] = !checks[24]} checked={checks[24]}>
         <label for="q24">25. Do you like roller coasters?</label>
         <br>
        <br>
        <button type="button" id="submit" on:click={() => {
           handleSubmit();
           showPop();
        }}>Submit</button>
        <button type="button" id="reset" on:click={() => {
            reset();
         }}>Reset</button>
    </form>
    <p id="output">Your score is {total}</p>
    <div class = "results">
        <dialog id="dresult" bind:this={dialog}>
            {#if total > 0}
                <img alt="No found" src={alpha} />
                <p>YOUR AURA IS {total}</p>
                <p>Congratualions you are offically a SIGMA</p>
            {:else}
            <img alt="No found" src={beta} />
                <p>YOUR AURA IS {total}</p>
                <p>You are not a sigma, you are a beta ... </p>
            {/if}
            <button type="button" on:click={() => {
                closePop();
            }}>Exit</button>
             <button type="button" on:click={() => {
                 share();
                }}>Share</button>
        </dialog>
    </div>
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

