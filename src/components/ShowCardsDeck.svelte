<script>
    let cardDeckName = 'Oceanography';
    let cardNumber = 19;
    let cardCountMax = 32;
</script>

<div class="card-deck">
    <h1>Studying: <span>{cardDeckName}</span></h1>
    <h2>{cardNumber} / {cardCountMax} <i class="fa fa-random" aria-hidden="true"></i></h2>
    <div class="grid-container">
        <div class="left"> <i class="fa fa-angle-left fa-4x" aria-hidden="true"></i> </div>
        <div class="mid">
            <div class="mid-card-text">
                <p>
                    What % of the earth’s surface is covered with oceans?
                </p>
                <div class="three-dots"><i class="fa fa-ellipsis-h fa-2x" aria-hidden="true"></i></div>
            </div>
        </div>
        <div class="right"><i class="fa fa-angle-right fa-4x" aria-hidden="true"></i></div>
    </div>
</div>

<style>
    .three-dots {
       display: flex;
       justify-content: right;
       padding-right: 25px;
       padding-bottom: 12px;
    }
    .mid-card-text {
        background: #F4F9FF 0% 0% no-repeat padding-box;
        border-radius: 13px;
        opacity: 1;
    }
    .left {
        display: grid;
        justify-content: center;
        align-content: center;
    }
    .right {
        display: grid;
        justify-content: center;
        align-content: center;
    }
    .mid-card-text p {
        padding: 35px 35px 0 35px;
        min-height: 350px;
        color: var(--unnamed-color-5f5f5f);
        text-align: left;
        font: normal normal normal 14px/19px Open Sans;
        letter-spacing: 0px;
        color: #5F5F5F;
        opacity: 1;
    }
    .grid-container {
    display: grid;
    grid-template-columns: 50px 600px 50px;
    grid-template-rows: 1fr;
    gap: 0px 0px;
    grid-template-areas:
        "left mid right";
    }
    .card-deck {
        color: var(--unnamed-color-5f5f5f);
        letter-spacing: 0px;
        width: 700px;
        height: 581px;
        background: #ffffff 0% 0% no-repeat padding-box;
        border-radius: 30px;
        opacity: 1;
    }
    .card-deck h1 {
        font: normal normal 600 18px/24px Open Sans;
        padding-top: 35px;
        text-align: center;
    }
    .card-deck h2 {
        padding:  20px;
        color: var(--unnamed-color-5f5f5f);
        text-align: left;
        font: normal normal 600 16px/22px Open Sans;
        letter-spacing: 0px;
        color: #5F5F5F;
        opacity: 1;
        text-align: center;
    }
    .card-deck span {
        font: normal normal bold 18px/24px Open Sans;
    }
</style>
