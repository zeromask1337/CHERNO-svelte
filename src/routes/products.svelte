<script>
    import Article from "../components/Article.svelte";

    async function getPosts() {
        let response = await fetch("https://jsonplaceholder.typicode.com/posts?_start=0&_limit=5");
        let json = await response.json();
        return json;
    }
    const promise = getPosts();
</script>


<Article title="Продукты">
    {#await promise}
        <p>Loading...</p>
    {:then posts}
        <p>В данном разделе приводятся описания готовых программ, разработанных ЗАО ИНПРО-1. Если у Вас появятся вопросы, их можно задать менеджеру по телефону +7 (495) 222-69-51. При необходимости можно организовать демонстрацию программы на реальной базе данных.</p>
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

<style lang="scss">
    @import "../base";

    p {
        margin-bottom: 20px;
    }

    .news-card {
        max-width: 700px;
        margin-bottom: 30px;

        display: grid;
    }

    .news-card img {
        padding: 10px 0;
    }

    @media (min-width: $ipad) {
        .news-card {
            margin-bottom: 30px;

            display: grid;
            grid-template-columns: 1fr 1fr;
            grid-template-rows: 1fr 1fr;
        }

        .news-card img {
            padding: 10px 0;

            grid-row: 1/3
        }

        .news-card h3 {
            grid-row: 1/2;
            grid-column: 2/3;
        }

        .news-card p {
            grid-row: 2/3;
            grid-column: 2/3;
        }
    }
</style>
