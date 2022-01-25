<script>
    import Info from './components/info.svelte';
    import Main from './components/main.svelte';
    import Footer from './components/footer.svelte';

    const cardInfo = {
        name: 'Laura Smith',
        title: 'Full Stack Developer',
        website: 'laurasmith.website',
        email: 'laurasmith@svelte.dev',
        imgPath: 'https://i.imgur.com/So04lBN.png',
    };

    const cardAbout = {
        about: `I am a frontend developer with a particular interest in making things simple and automating daily tasks. I try to keep up with security and best practices, and am always looking for new things to learn.`,
        interests: `Food expert. Music scholar. Reader. Internet fanatic. Bacon buff. Entrepreneur. Travel geek. Pop culture ninja. Coffee fanatic.`,
    };

    const socials = [
        { name: 'twitter', link: 'laura.smith', filename: 'twtr.png' },
        { name: 'facebook', link: 'laura.smith', filename: 'fb.png' },
        {
            name: 'instagram',
            link: 'laura.smith',
            filename: 'ig.png',
        },
        { name: 'linkedin', link: 'smith-laura', filename: 'link.png' },
        { name: 'github', link: 'laura.smith', filename: 'git.png' },
    ];
</script>

<main>
    <h1>Customize your Card</h1>
</main>
<hero>
    <div>
        <Info {...cardInfo} />
        <Main {...cardAbout} />
        <Footer {socials} />
    </div>
    <section>
        <label>
            <p>Name:</p>
            <input type="text" placeholder="Name" bind:value={cardInfo.name} />
        </label>
        <label>
            <p>Title:</p>
            <input
                type="text"
                placeholder="Title"
                bind:value={cardInfo.title}
            />
        </label>
        <label>
            <p>Website:</p>
            <input
                type="text"
                placeholder="Website"
                bind:value={cardInfo.website}
            />
        </label>
        <label>
            <p>Email:</p>
            <input
                type="text"
                placeholder="email"
                bind:value={cardInfo.email}
            />
        </label>
        <label>
            <p>Image link:</p>
            <input
                type="text"
                placeholder="img path"
                bind:value={cardInfo.imgPath}
            />
        </label>
        <label>
            <p>About me:</p>
            <textarea name="about" bind:value={cardAbout.about} />
        </label>
        <label>
            <p>Interests:</p>
            <textarea name="interests" bind:value={cardAbout.interests} />
        </label>
        {#each socials as social}
            <label>
                <p>{social.name}:</p>
                <input
                    type="text"
                    placeholder={`${social.name}`}
                    bind:value={social.link}
                />
            </label>
        {/each}
    </section>
</hero>

<style>
    :global(body) {
        margin: 0px;
        font-family: Inter, sans-serif;
        background: #23252c;
    }
    hero {
        display: flex;
        justify-content: space-evenly;
    }
    p {
        color: white;
    }

    div {
        /* display: block; */
        background: #1a1b21;
        border-radius: 9px;
        width: 317px;
        max-width: 317px;
        /* margin: 10px auto; */
    }

    section {
        display: flex;
        flex-flow: column nowrap;
        width: 30%;
    }

    main {
        text-align: center;
        padding: 1em;
        max-width: 240px;
        margin: 0 auto;
    }

    h1 {
        color: #ff3e00;
        text-transform: uppercase;
        font-size: 3em;
        font-weight: 100;
    }

    label {
        display: flex;
        align-items: center;
    }
    label p {
        width: 20%;
    }
    input {
        margin: 6px;
        width: 45%;
        height: 30px;
    }
    textarea {
        margin: 6px;
        width: 100%;
        height: 100px;
    }
    @media (min-width: 640px) {
        main {
            max-width: none;
        }
    }

    @media only screen and (max-width: 640px) {
        hero {
            flex-direction: column;
            align-items: center;
        }
        section {
            margin-top: 3em;
            width: 500px;
        }
        input {
            width: 100%;
        }

        label {
            width: 100%;
            justify-content: space-evenly;
        }
    }
</style>
