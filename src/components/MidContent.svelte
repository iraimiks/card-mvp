<script>
    let hours = 0;
    let minutes = 0;
    let totalNumberCards = 10;
</script>

<div class="mid-content">
    <div class="mid-content-right">
        <h2>Welcome, Sara!</h2>
        <p>
            We are happy to see You! We created for You 2 folders with cards to
            begin with. Feel free to add Your own card or folder by clicking the
            plus sign on the left side of the screen. And wish You happy
            learning!
        </p>
    </div>
    <div class="mid-content-left">
        <h3>Your Statistics</h3>
            <div class="mid-content-internal">
                <div class="mid-inter-left">
                    <h4>Time spent on studying:</h4>
                    <p><span>{hours}</span> hours, <span>{minutes}</span> minutes</p>
                </div>
                <div class="mid-inter-right">
                    <h4>Total number of cards:</h4>
                    <p><span>{totalNumberCards}</span></p>
                </div>
            </div>
    </div>
</div>

<style>
    .mid-content {
        display: flex;
        height: 218px;
    }
    .mid-content-right {
        width: 28%;
        padding: 35px 0 35px 35px;
    }
    .mid-content-right h2 {
        padding-bottom: 19px;
    }
    .mid-content-left {
        display: flex;
        flex-direction: column;
        padding: 40px 0 0 42px;
    }
    .mid-content-internal{
        display: flex;
        flex-direction: row;
    }
    .mid-inter-left {
        margin: 0 25px 0 0
    }
    .mid-inter-left h4, .mid-inter-right h4{
        padding: 0 0 10px 0;
    }
    .mid-inter-right {
        margin: 0 0 0 25px
    }
    .mid-content-left h4 {
        padding-top: 19px;
    }
</style>
