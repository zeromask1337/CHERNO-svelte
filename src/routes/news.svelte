<script>
    import Article from "../components/Article.svelte";

    async function getPosts() {
        let response = await fetch("https://jsonplaceholder.typicode.com/posts?_start=0&_limit=10");
        let json = await response.json();
        return json;
    }
    const promise = getPosts();
</script>


<Article title="Новости">
    {#await promise}
        <p>Loading...</p>
    {:then posts}
        {#each posts as post}
            <div class="news-card">
                <h3>{post.title}</h3>
                <img src="https://picsum.photos/300/200" alt="">
                <p>{post.body}</p>
            </div>
        {/each}
    {:catch error}
        <p style="color: red">{error.message}</p>
    {/await}
</Article>

<style>
    .news-card {
        margin-bottom: 30px;

        display: grid;
    }

    .news-card img {
        padding: 10px 0;
    }
</style>
