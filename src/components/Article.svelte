<script>
    export let title;
</script>

<article>
    <h1>{title}</h1>
    <slot></slot>
</article>

<style>
    article {
        padding: 20px 10px 20px 20px;

        margin-bottom: 30px;
    }

    h1 {
        padding-bottom: 10px;
    }
</style>