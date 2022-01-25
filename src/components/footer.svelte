<script>
    export let socials;
    console.log(socials);
</script>

<div>
    {#each socials as social}
        {#if social.name !== 'linkedin'}
            <a
                href={`https://${social.name}.com/${social.link}`}
                target="_blank"
            >
                <img src={`../images/${social.filename}`} alt="" />
            </a>
        {:else}
            <a
                href={`https://${social.name}.com/in/${social.link}`}
                target="_blank"
            >
                <img src={`../images/${social.filename}`} alt="" />
            </a>
        {/if}
    {/each}
</div>

<style>
    div {
        border-radius: 9px;
        background: #161619;
        padding: 20px 40px;
        display: flex;
        justify-content: space-between;
    }
    img {
        width: 25px;
    }
</style>
