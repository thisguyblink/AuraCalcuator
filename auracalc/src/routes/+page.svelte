<script>
    import alpha from '$lib/assets/alpha wolf.jpeg';
    import beta from '$lib/assets/beta wolf.gif';
    import tape from '$lib/assets/tape texture.png';
    const values = [-50, 100, 150, -50, -25, -100, -150, -250, 500, 50, 200, -300, 50, 250, 75, 100, -300, -50, 100, -125, -200, 150, 75, 50, -1000, -200, 50, -150, 300, 2000, 200, -300, 325, 5000, 1, -2000, 800, -100, -50, -125, 50, 500, 2000, -30, -500, 350, 100, 1500, 225, -1250];
    let out = 'Cowabunga';
    let total = 0;
    let dialog;
    let checks = [false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false];

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
            output = "I am officially a SIGMA! I am proud to announce that my Aura is " + total + "!!!\nSee if you're a Sigma too\n" + "aura.gmoneymoves.com";
            navigator.clipboard.writeText(output);
        }
        else {
            output = "I am not a sigma :( I regret to inform you that my aura is " + total + "\nHopefully you're not a beta too\n" + "aura.gmoneymoves.com";
            navigator.clipboard.writeText(output);
        }
        window.confirm("Results have been copied to clipboard!");
    }
    
</script>
<body>
    <div class="texture">
        <img alt="No found" id="tape"src={tape}>
    </div>
<div class = "header">
    <h1>Form AC-11:<br>Aura Calculator</h1>
    <h3 id = "gov">&#9888 Government Sanctioned Aura Testing &#9888</h3>
    <p class="description">This is a test designed to calculate your Aura based on your actions. If there isn't a time frame listed use best judgment.<br> Don't lie, we will know. We are watching. <br>Happy Testing, <br> G Money Moves Inc. </p>
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
         <input type="checkbox" id="q37" on:change={() => checks[37] = !checks[37]} checked={checks[37]}>
         <label for="q37">38. Get caught staring at someone?</label>
         <br>
         <input type="checkbox" id="q38" on:change={() => checks[38] = !checks[38]} checked={checks[38]}>
         <label for="q38">39. Card declined?</label>
         <br>
         <input type="checkbox" id="q39" on:change={() => checks[39] = !checks[39]} checked={checks[39]}>
         <label for="q39">40. Coughed after taking a hit?</label>
         <br>
         <input type="checkbox" id="q40" on:change={() => checks[40] = !checks[40]} checked={checks[40]}>
         <label for="q40">41. Cooked a homemade meal in the past week?</label>
         <br>
         <input type="checkbox" id="q41" on:change={() => checks[41] = !checks[41]} checked={checks[41]}>
         <label for="q41">42. Got rizzed up?</label>
         <br>
         <input type="checkbox" id="q42" on:change={() => checks[42] = !checks[42]} checked={checks[42]}>
         <label for="q42">43. Have a record for anything?</label>
         <br>
         <input type="checkbox" id="q43" on:change={() => checks[43] = !checks[43]} checked={checks[43]}>
         <label for="q43">44. Are you a <i>certified</i> hater?</label>
         <br>
         <input type="checkbox" id="q44" on:change={() => checks[44] = !checks[44]} checked={checks[44]}>
         <label for="q44">45. Lost something and spent more than an hour looking for it?</label>
         <br>
         <input type="checkbox" id="q45" on:change={() => checks[45] = !checks[45]} checked={checks[45]}>
         <label for="q45">46. Listen to Jazz?</label>
         <br>
         <input type="checkbox" id="q46" on:change={() => checks[46] = !checks[46]} checked={checks[46]}>
         <label for="q46">47. You think Dave's Hot Chicken is better than Canes?</label>
         <br>
         <input type="checkbox" id="q47" on:change={() => checks[47] = !checks[47]} checked={checks[47]}>
         <label for="q47">48. Kendrick is better than Drake(in every way)?</label>
         <br>
         <input type="checkbox" id="q48" on:change={() => checks[48] = !checks[48]} checked={checks[48]}>
         <label for="q48">49. Do you even lift bro?</label>
         <br>
         <input type="checkbox" id="q49" on:change={() => checks[49] = !checks[49]} checked={checks[49]}>
         <label for="q49">50. Watched a horror movie and got scared?</label>
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
    <p id="complaints">If you don't like your score, you can email betacompliants@gmoneymoves.com or DM @gmoneymoves</p>
    <a id="github" href='https://github.com/thisguyblink/AuraCalcuator'>
        <p>Project is Now Finished<br> Github Repo found here!</p>
    </a>
    <div class = "results">
        <dialog id="dresult" bind:this={dialog}>
            <button type="button" id="exit" on:click={() => {
                closePop();
            }}>X</button>
            <br>
            <div class="popup">
                {#if total > 0}
                <img alt="No found" id="alpha" src={alpha} />
                <p class="aura">AURA: {total}</p>
                <p class="aura">LEVEL: SIGMA</p>
                {:else}
                <img alt="No found" id="beta" src={beta} />
                <p class ="aura">AURA: {total}</p>
                <p class="aura">level: beta </p>
                {/if}
                <button type="button" id="share" on:click={() => {
                    share();
                }}>Share</button>
            </div>
        </dialog>
    </div>
</div>
</body>
<style>
    .header {
        padding-top: 2rem;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        font-weight: 900;
        font-size: 1.25rem;
        text-align: center;
    }
    .questionList {
        padding-top: 3rem;
        padding-left: 3rem;
        display: flex;
        justify-content: center;
        left: 10%;
        flex-direction: column;
        font-size: 1.25rem;
        font-weight: 400;
    }
    #submit {
        background-color: #264653;
        color: white;
        border-color: #faedcd;
        font-size: 3.5rem;
        border-radius: 1rem;
        width: 17rem;
        height: 6rem;
        border-width: .5rem;
    }
    #submit:hover {
        color: black;
        background-color: #faedcd;
        border-color: #d4a373;
        border-width: .5rem;
    }
    #reset {
        background-color: #e63946;
        color: white;
        border-color: #faedcd;
        font-size: 2rem;
        border-radius: 1rem;
        width: 10rem;
        height: 3rem;
        margin-top: 2rem;
    }
    #reset:hover {
        color: #e63946;
        background-color: #faedcd;
        border-color: #d4a373;
    }
    #output {
        height: auto;
        width: auto;
        padding: 2rem;
        background-color: #a8dadc;
        color: #1d3557;
        border: 3px solid #1d3557;
        align-self: center;
        text-align: center;
        font-size: 2rem;
        border-radius:  2rem;
    }
    #alpha {
        height: 25rem;
        width: auto;
        border-radius: 20px;
    }
    #beta {
        height: 10rem;
        width: auto;
        border-radius: 7px;
    }
    #exit {
        position: relative;
        left: 90%;
        justify-content: end;
        margin-bottom: 1rem;
        font-size: 1.5rem;
        border: 3px solid #1d3557;
        border-radius: 5px;
        background-color: #faedcd;
    }
    .popup {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        backdrop-filter: blur(3px);
    }
    .buttons {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        left: 50%;
    }

    * {
        font-family: "Public Sans", sans-serif;
        font-optical-sizing: auto;
        font-style: normal;
    }
    .description {
        max-width: 30rem;
        width: auto;
        flex-wrap: wrap;
        font-weight: 400;
        font-size: 1rem;
    }
    #complaints {
        display: flex;
        max-width: 30rem;
        width: auto;
        padding-bottom: 2rem;
        padding-top: 1rem;
        flex-direction: column;
        font-size: 1.25rem;
        text-align: center;
        align-self: center;
        justify-content: center;
    }
    #gov {
        text-align: center;
        align-items: center;
        justify-content: center;
    }
    #dresult {
        border: 5px solid #1d3557;
        border-radius: 15px;
        background-color: #d4a373;
    }
    .aura {
        margin: 1rem;
        font-size: 3rem;
        font-weight: 900;
    }
    #share {
        font-size: 1.5rem;
        font-weight: 300;
        border: 3px solid #264653;
        border-radius: 5px;
        background-color: #faedcd;
    }
    .results {
        backdrop-filter: blur(100px);
    }
    #tape {
        position: absolute;
        z-index: -1;
        opacity: 23%;
        height: 310%;
        width: 97%;
        object-fit: cover;
        filter: blur(6px);
        margin-left: .5rem
    }
    #github {
        align-items: center;
        text-decoration: none;
        justify-content: center;
        text-align: center;
        display: flex;
        font-weight: 700;
        color: #1d3557;
        font-size: 1.5rem;
    }
    #github:hover {
        text-decoration: underline;
    }
</style>