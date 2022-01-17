<nav>
    <ul>
        <a href="/"><img src="" alt="logo"></a>
        <li><a href="/news">Новости</a></li>
        <li><a href="/articles">Статьи</a></li>
        <li><a href="/products">Продукция</a></li>
        <li><a href="/services">Услуги</a></li>
        <li><a href="/contacts">Контакты</a></li>
        <li><a href="about">О нас</a></li>
    </ul>
</nav>

<style lang="scss">
    @import "../base";

    :global(#svelte, nav) {
      width: 100vw;
      height: 53px;
    }

    ul {
        display: flex;
        flex-flow: row;

        list-style-type: none;

        & > * {
            padding-right: 10px;
        }

        @media (min-width: $mobile) {
          background-color: red;
        }
    }

</style>