<script>
    export let about;
    export let interests;
</script>

<div>
    <h3>About</h3>
    <p>
        {about}
    </p>
    <h3>Interests</h3>
    <p>{interests}</p>
</div>

<style>
    div {
        margin: 30px 0 0 0;
        padding-bottom: 30px;
    }

    h3 {
        color: #f5f5f5;
        font-size: 16px;
        font-weight: bold;
        margin: 0px 0 0 34px;
        padding: 0;
    }

    p {
        color: #dcdcdc;
        font-size: 10.24px;
        padding: 0;
        margin: 12px 0 15px 34px;
        max-width: 247px;
    }
</style>
