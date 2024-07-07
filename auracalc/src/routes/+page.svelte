<script>
    const values = [-50, 100, 150, -50, -25, -100, -150, -250, 500, 50, 200, -300, 50, 250, 75, 100, -300, -50, 100, -125, -200, 150, 75, 50, -1000, -200, 50, -150, 300, 2000, 200, -300, 325, 5000, 1, -2000, 800];
    let out = 'Cowabunga';
    let total = 0;
    let dialog;
    let checks = [false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false];
    import alpha from '$lib/assets/alpha wolf.jpeg';
    import beta from '$lib/assets/beta wolf.gif'

    function handleSubmit() {
        out = values[0];
        total = 0;
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
        total = 0;
        // location.reload();
    }
    function showPop() {
        dialog.showModal();
    }
    function closePop() {
        dialog.close();
    }
    function share() {
        var output;
        if (total > 0) {
            output = "I am officially a SIGMA! I am proud to announce that my Aura is " + total + "\nSee if you're a Sigma too\n" + "aura.gmoneymoves.com";
            navigator.clipboard.writeText(output);
        }
        else {
            output = "I am not a sigma :( I regret to inform you that my aura is " + total + "\nHopefully you're not a beta too\n" + "aura.gmoneymoves.com";
            navigator.clipboard.writeText(output);
        }
        window.confirm("Results have been copied to clipboard!");
    }
    
</script>

<div class = header>
    <h1>Aura Calculator</h1>
    <h3>Take it if you dare!</h3>
    <h3>Are you a SIGMA or beta...</h3>
</div>
<div class ="questionList">
    <form class="questionForm" method="POST" action="?/submission">
         <input type="checkbox" id="q0" on:change={() => checks[0] = !checks[0]}>
         <label for="q0">1. Tripped on something in the past week?</label>
         <br>
         <input type="checkbox" id="q1" on:change={() => checks[1] = !checks[1]} checked={checks[1]}>
         <label for="q1">2. Rizzed up a person in the past week?</label>
         <br>
         <input type="checkbox" id="q2" on:change={() => checks[2] = !checks[2]} checked={checks[2]}>
         <label for="q2">3. Jaywalked but didn't have to run across?</label>
         <br>
         <input type="checkbox" id="q3" on:change={() => checks[3] = !checks[3]} checked={checks[3]}>
         <label for="q3">4. Stuttered in the past day?</label>
         <br>
         <input type="checkbox" id="q4" on:change={() => checks[4] = !checks[4]} checked={checks[4]}>
         <label for="q4">5. Threw up?</label>
         <br>
         <input type="checkbox" id="q5" on:change={() => checks[5] = !checks[5]} checked={checks[5]}>
         <label for="q5">6. Dropped something?</label>
         <br>
         <input type="checkbox" id="q6" on:change={() => checks[6] = !checks[6]} checked={checks[6]}>
         <label for="q6">7. Sneezed more than 3 times in a row?</label>
         <br>
         <input type="checkbox" id="q7" on:change={() => checks[7] = !checks[7]} checked={checks[7]}>
         <label for="q7">8. Got lower than a 50% on a test after the curve?</label>
         <br>
         <input type="checkbox" id="q8" on:change={() => checks[8] = !checks[8]} checked={checks[8]}>
         <label for="q8">9. Dropped something but caught it before it hit the ground?</label>
         <br>
         <input type="checkbox" id="q9" on:change={() => checks[9] = !checks[9]} checked={checks[9]}>
         <label for="q9">10. Got something for free?</label>
         <br>
         <input type="checkbox" id="q10" on:change={() => checks[10] = !checks[10]} checked={checks[10]}>
         <label for="q10">11. Sports team won a championship, not including the celtics?</label>
         <br>
         <input type="checkbox" id="q11" on:change={() => checks[11] = !checks[11]} checked={checks[11]}>
         <label for="q11">12. Sports team lost in the championship?</label>
         <br>
         <input type="checkbox" id="q12" on:change={() => checks[12] = !checks[12]} checked={checks[12]}>
         <label for="q12">13. BAC above .1 in the last month?</label>
         <br>
         <input type="checkbox" id="q13" on:change={() => checks[13] = !checks[13]} checked={checks[13]}>
         <label for="q13">14. Almost died but didn't?</label>
         <br>
         <input type="checkbox" id="q14" on:change={() => checks[14] = !checks[14]} checked={checks[14]}>
         <label for="q14">15. Won an award?</label>
         <br>
         <input type="checkbox" id="q15" on:change={() => checks[15] = !checks[15]} checked={checks[15]}>
         <label for="q15">16. Volunteered or donated to charity?</label>
         <br>
         <input type="checkbox" id="q16" on:change={() => checks[16] = !checks[16]} checked={checks[16]}>
         <label for="q16">17. Got rejected, for anything?</label>
         <br>
         <input type="checkbox" id="q17" on:change={() => checks[17] = !checks[17]} checked={checks[17]}>
         <label for="q17">18. Had a bad picture taken of you?</label>
         <br>
         <input type="checkbox" id="q18" on:change={() => checks[18] = !checks[18]} checked={checks[18]}>
         <label for="q18">19. Friend took a good candid picture?</label>
         <br>
         <input type="checkbox" id="q19" on:change={() => checks[19] = !checks[19]} checked={checks[19]}>
         <label for="q19">20. Burnt something while cooking, literally or figureatively?</label>
         <br>
         <input type="checkbox" id="q20" on:change={() => checks[20] = !checks[20]} checked={checks[20]}>
         <label for="q20">21. Mispelt a word?</label>
         <br>
         <input type="checkbox" id="q21" on:change={() => checks[21] = !checks[21]} checked={checks[21]}>
         <label for="q21">22. Got a paycheck this week?</label>
         <br>
         <input type="checkbox" id="q22" on:change={() => checks[22] = !checks[22]} checked={checks[22]}>
         <label for="q22">23. Watched a GOOD movie, iykyk!?!?</label>
         <br>
         <input type="checkbox" id="q23" on:change={() => checks[23] = !checks[23]} checked={checks[23]}>
         <label for="q23">24. Finished a project, and it works?</label>
         <br>
         <input type="checkbox" id="q24" on:change={() => checks[24] = !checks[24]} checked={checks[24]}>
         <label for="q24">25. Sold your soul or moral for money #sellout?</label>
         <br>
         <input type="checkbox" id="q25" on:change={() => checks[25] = !checks[25]} checked={checks[25]}>
         <label for="q25">26. Broke something?</label>
         <br>
         <input type="checkbox" id="q26" on:change={() => checks[26] = !checks[26]} checked={checks[26]}>
         <label for="q26">27. Cried?</label>
         <br>
         <input type="checkbox" id="q27" on:change={() => checks[27] = !checks[27]} checked={checks[27]}>
         <label for="q27">28. Cried because of anouther person?</label>
         <br>
         <input type="checkbox" id="q28" on:change={() => checks[28] = !checks[28]} checked={checks[28]}>
         <label for="q28">29. Receive a compliment?</label>
         <br>
         <input type="checkbox" id="q29" on:change={() => checks[29] = !checks[29]} checked={checks[29]}>
         <label for="q29">30. Your crush complimented you?</label>
         <br>
         <input type="checkbox" id="q30" on:change={() => checks[30] = !checks[30]} checked={checks[30]}>
         <label for="q30">31. Got on the jumbotron at a sports game?</label>
         <br>
         <input type="checkbox" id="q31" on:change={() => checks[31] = !checks[31]} checked={checks[31]}>
         <label for="q31">32. Lost a bet?</label>
         <br>
         <input type="checkbox" id="q32" on:change={() => checks[32] = !checks[32]} checked={checks[32]}>
         <label for="q32">33. Won a bet?</label>
         <br>
         <input type="checkbox" id="q33" on:change={() => checks[33] = !checks[33]} checked={checks[33]}>
         <label for="q33">34. Listen to MF DOOM?</label>
         <br>
         <input type="checkbox" id="q34" on:change={() => checks[34] = !checks[34]} checked={checks[34]}>
         <label for="q34">35. Swiftie?</label>
         <br>
         <input type="checkbox" id="q35" on:change={() => checks[35] = !checks[35]} checked={checks[35]}>
         <label for="q35">36. Likes pineapple on Pizza?(Disgusting)</label>
         <br>
         <input type="checkbox" id="q36" on:change={() => checks[36] = !checks[36]} checked={checks[36]}>
         <label for="q36">37. Clutch up in any game?</label>
         <br>

        <br>
        <div class="buttons">
            <button type="button" id="submit" on:click={() => {
                handleSubmit();
                showPop();
            }}>Submit</button>
            <br>
            <button type="button" id="reset" on:click={() => {
                reset();
            }}>Reset</button>
        </div>
    </form>
    <p id="output">Your score is {total}</p>
    <div class = "results">
        <dialog id="dresult" bind:this={dialog}>
            <button type="button" id="exit" on:click={() => {
                closePop();
            }}>X</button>
            <br>
            <div class="popup">
                {#if total > 0}
                <img alt="No found" id="alpha" src={alpha} />
                <p>YOUR AURA IS {total}</p>
                <p>Congratualions you are offically a SIGMA</p>
                {:else}
                <img alt="No found" id="beta" src={beta} />
                <p>YOUR AURA IS {total}</p>
                <p>You are not a sigma, you are a beta ... </p>
                {/if}
                <button type="button" on:click={() => {
                    share();
                }}>Share</button>
            </div>
        </dialog>
    </div>
</div>
<style>
    .questionForm {
        background-color: #CCCCDD;
    }
    .header {
        padding-top: 3rem;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
    }
    h1{
        color: white;
        font-family: 'Limelight' cursive;

    }
    .questionList {
        padding-top: 3rem;
        display: flex;
        justify-content: center;
        margin-left: 20px;
        /*align-items: center;*/
        flex-direction: column;
        font-size: 1.25rem;
        font-family: 'Inria Serif', serif;
    }
    h3{
        font-family: 'Jeju Hallasan', sans-serif;
    }
    #submit {
        background-color: rgb(172, 98, 233);
        border-color: azure;
        color: white;
        font-size: medium;
    }
    #output {
        border: 3px solid purple;
        height: 5rem;
        width: 10rem;
        background-color: beige;
        align-self: center;
        text-align: center;
        font-size: 2rem;
    }
    #alpha {
        height: 30rem;
        width: auto;
    }
    #beta {
        height: 10rem;
        width: auto;
    }
    #exit {
        position: relative;
        left: 90%;
        justify-content: end;
        margin-bottom: 1rem;
        font-size: 1.5rem;
    }
    .popup {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
    }
    .buttons {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        left: 50%;
    }

</style>