<script>
    import Article from "../components/Article.svelte";
</script>

<Article title="">
    <p>Компания "Информационные проекты" с более чем 15 летним опытом работы на рынке программного обеспечения предлагает решения:</p>
    <br>
    <ul>
        <li><a href="http://inproekt.ru/index.php?act=viewpg_prod&id=2">Для гостиничного бизнеса и онлайн
            бронирования</a></li>
        <li><a href="http://inproekt.ru/index.php?act=viewpg_prod&id=1">Для пищевого производства</a></li>
        <li><a href="http://inproekt.ru/index.php?act=viewpg_prod&id=4">Для организации дистанционного обучения и
            тестирования</a></li>
        <li><a href="http://inproekt.ru/index.php?act=viewpg_prod&id=3">Для подготовки самоописываемых бланков
            соцопросов и их ввода на основе технологии сканирования</a></li>
        <li><a href="http://inproekt.ru/index.php?act=viewpg_prod&id=5">Для ВУЗов</a></li>
    </ul>
    <br>
    Большинство решений реализовано на основе WEB-технологий и свободного программного обеспечения. В компании работают специалисты, имеющие большой практический опыт, в том числе программисты, авторы учебных материалов, корректоры, методисты, преподаватели ВУЗов, дизайнеры, психологи. Одним из направлений деятельности компании является разработка программных продуктов (в том числе сайтов и портальных решений) «под заказ».
</Article>


<style lang="scss">
    :global(body) {
      min-height: 100vh;

      font-family: 'Montserrat', sans-serif;
      color: black;
    }

    :global(*) {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      text-decoration: none;
      list-style-type: none;
    }

    :global(button) {
      all: unset;
    }

    :global(a) {
        color: inherit;
    }

    ul li {
      list-style-type: disc;
      list-style-position: inside;
    }
</style>
