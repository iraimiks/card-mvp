<script>
</script>

<div class="grid-container">
    <div class="left">Left</div>
    <div class="center">
        <i class="fa fa-search icon" aria-hidden="true" />
        <input
            class="search-input-header"
            type="text"
            placeholder="Search for a card or a folder, by the key word"
        />
    </div>
    <div class="right">Right</div>
</div>

<style>
    .grid-container {
        display: grid;
        grid-template-columns: 90px 2.2fr 80px;
        grid-template-rows: 100px;
        gap: 0px 0px;
        grid-template-areas: "left center right";
        align-items: center;
    }
    .left {
        grid-area: left;
    }
    .center {
        grid-area: center;
    }
    .right {
        grid-area: right;
    }
    .search-input-header {
        width: 382px;
        height: 40px;
        background: #ffffff 0% 0% no-repeat padding-box;
        border-radius: 14px;
        opacity: 1;
    }
    .icon {
        padding: 13px 20px 13px;
        min-width: 40px;
    }
    .center i {
        position: absolute;
    }
    input {
        text-indent:48px;
    }
    input::placeholder {
        color: var(--unnamed-color-b9b9b9);
        font-size: 14px;
        text-align: left;
        letter-spacing: 0px;
        padding: 10px 11px 52px;
    }
</style>
