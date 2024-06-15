<script>
    // document.getElementById('submitButton').addEventListener('click', function() {
    //     const checkboxes = document.querySelectorAll('input[type="checkbox"]');
    //   let totalValue = 0;
    //   checkboxes.forEach(checkbox => {
    //     if (checkbox.checked) {
    //       totalValue += parseInt(checkbox.value);
    //     }
    //   });
    // });
</script>

<div class = header>
    <h1>Aura Calcualator</h1>
    <h3>Take it if you dare!</h3>
    <h3>Are you a Alpha or a Sigma...</h3>
</div>
<div class ="questionList">
    <div class = question>
        <label class="custom-checkbox">
            <input type="checkbox" value="100">
            1. Have you rizzed up at least 10 people in the last week?
        </label>
    </div>
    <div class = question>
        <label class="custom-checkbox">
            <input type="checkbox" value="15">
            2. Finished something earlier than expected?
        </label>
    </div>
    <div class = question>
        <label class="custom-checkbox">
            <input type="checkbox" value="-60">
            3. Was late at least once?
        </label>
    </div>
    <div class = question>
        <label class="custom-checkbox">
            <input type="checkbox" value="-450">
            4. Got a flat tire?
        </label>
    </div>
    <div class = question>
        <label class="custom-checkbox">
            <input type="checkbox" value="-100">
            5. Dropped something?
        </label>
    </div>
    <div class = question>
        <label class="custom-checkbox">
            <input type="checkbox" value="4500">
            6. Almost died but didn't?
        </label>
    </div>
    
    <span></span>
    <button id ="submitButton">Submit</button>
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
    .checkbox:hover {
        background-color: black;
    }

</style>

