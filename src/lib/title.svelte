<script>
    export let title = "Page title"
    
    const updateTitle = () => {
        title = "Page Title updated!";
    }
</script>

<div class="title">
    <!-- <img src="/favicon.png" alt="" class="src"> -->
    <h1>{title}</h1>
    <button on:click={updateTitle}> Update title</button>
</div>

<style>
    .title {
        display: inline-block;
        margin: 0 auto;
        text-align: center;
    }
</style>