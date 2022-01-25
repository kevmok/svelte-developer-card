<script>
    export let name;
    export let title;
    export let website;
    export let email;
    export let imgPath;
</script>

<img src={imgPath} alt="profile-pic" />
<div>
    <h2>{name}</h2>
    <h5>{title}</h5>
    <h6><a href={`https://${website}`} target="_blank">{website}</a></h6>
    <button><a href={`mailto:${email}`}>Email</a></button>
</div>

<style>
    div {
        text-align: center;
    }
    img {
        width: 317px;
        border-radius: 9px 9px 0 0;
    }
    h2 {
        color: white;
        margin: 20px 0 0 0;
        padding: 0;
        font-weight: 700;
    }
    h5 {
        margin: 5px 0 0 0;
        padding: 0;
        font-size: 12.8px;
        font-weight: 400;
        color: #f3bf99;
    }
    h6 {
        margin: 10px;
        padding: 0;
        font-size: 10.4px;
        font-weight: 400;
        color: #f5f5f5;
        transition-duration: 0.5s;
    }

    h6:hover {
        transform: scale(1.1);
    }
    a {
        text-decoration: none;
        color: inherit;
    }

    button {
        margin-top: 7px;
        width: 247px;
        padding: 8px;
        background: white;
        border: none;
        box-shadow: 0px 1px 2px rgba(0, 0, 0, 0.05);
        border-radius: 6px;
        font-size: 14px;
        color: #374151;
        font-weight: 500;

        cursor: pointer;

        transition-duration: 1s;
    }

    button:hover {
        background: #dd692f;
        border: none;
    }
</style>
