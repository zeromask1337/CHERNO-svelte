<script>
    async function getPhotos() {
        let response = await fetch("https://jsonplaceholder.typicode.com/photos?_start=0&_limit=10");
        let json = await response.json();
        return json;
    }
    const promise = getPhotos();
</script>

<aside class="news">
    {#await promise}
        <p>Loading...</p>
    {:then photos}
        <h2>Новости</h2>
        {#each photos as photo}
            <div class="photo-card">
                <span>{photo.id}</span>
                <p>{photo.title}</p>
                <img src={photo.thumbnailUrl} alt="">
            </div>
        {/each}
    {:catch error}
        <p style="color: red">{error.message}</p>
    {/await}
</aside>

<style lang="scss">
    @import "../base";

    h2 {
      margin-bottom: 20px;
    }

    aside {
      padding: 50px;

      background-color: #7CA982;
    }

    .photo-card {
        margin-bottom: 20px;

        display: flex;
        flex-flow: column;
    }

    .photo-card img {
        width: 200px;
        height: 140px;
    }

    @media (min-width: $ipad) {
        .photo-card img {
            width: 100px;
            height: 70px;
        }
    }
</style>