<script>
    import Header from "./components/Header.svelte";
    import MidContent from "./components/MidContent.svelte";
    import Card from "./components/Card.svelte";
    import Modal from "./uiengine/Modal.svelte";
    import ShowCardsDeck from "./components/ShowCardsDeck.svelte";
    let showModal = false;
</script>

<div class="right-nav-cross">
    <div>
        <i class="fa fa-plus-circle fa-2x fa-inverse" aria-hidden="true" />
    </div>
</div>
<div class="right-nav-bascket">
    <div>
        <i
            class="fa fa-archive fa-2x"
            aria-hidden="true"
            style="color:#126DEB"
        />
    </div>
</div>
<div class="grid-container">
    <div class="header">
        <Header />
    </div>
    <div class="mid-content mid-margin">
        <MidContent />
    </div>
    <div class="mid-main-content mid-margin-content">
        <a on:click={() => (showModal = true)}>
            <Card />
        </a>
        {#if showModal}
            <Modal on:close={() => (showModal = false)}>
                <ShowCardsDeck />
            </Modal>
        {/if}
    </div>
    <div class="footer">
        <h3>© 2021 All rights reserved</h3>
    </div>
</div>

<style>
    .mid-margin {
        margin: 0 30px 10px 90px;
    }
    .mid-margin-content {
        margin: 10px 30px 0 90px;
    }
    .grid-container {
        display: grid;
        grid-template-columns: 90px 1.7fr;
        grid-template-rows: 130px auto auto 78px;
        gap: 0px 0px;
        grid-template-areas:
            "header header"
            "mid-content mid-content"
            "mid-main-content mid-main-content"
            "footer footer";
        min-height: 100vh;
    }
    .footer {
        color: var(--unnamed-color-b9b9b9);
        text-align: center;
        font: normal normal normal 14px/19px Open Sans;
        letter-spacing: 0px;
        color: #b9b9b9;
        opacity: 1;
        align-self: center;
        justify-self: center;
        grid-area: footer;
        position: relative;
        bottom: 0;
        left: 0;
        right: 0;
    }
    .mid-main-content {
        grid-area: mid-main-content;
        background: #ffffff 0% 0% no-repeat padding-box;
        border-radius: 13px;
        min-height: 300px;
    }
    .mid-content {
        grid-area: mid-content;
        background: #ffffff 0% 0% no-repeat padding-box;
        border-radius: 13px;
        opacity: 1;
    }
    .header {
        grid-area: header;
        background: var(--unnamed-color-f0f2f4) 0% 0% no-repeat padding-box;
        background: #f0f2f4 0% 0% no-repeat padding-box;
        opacity: 1;
        backdrop-filter: blur(50px);
        -webkit-backdrop-filter: blur(50px);
    }
    .right-nav-cross {
        display: flex;
        justify-content: center;
        align-items: center;
        position: absolute;
        top: 130px;
        left: 0;
        width: 60px;
        height: 300px;
        background: var(--unnamed-color-126deb) 0% 0% no-repeat padding-box;
        border-radius: 0px 30px 30px 0px;
        opacity: 1;
        z-index: 11;
    }
    .right-nav-bascket {
        display: flex;
        justify-content: center;
        align-items: center;
        position: absolute;
        top: 450px;
        left: 0px;
        width: 60px;
        height: 108px;
        background: #ffffff 0% 0% no-repeat padding-box;
        border-radius: 0px 30px 30px 0px;
        opacity: 1;
    }
</style>
