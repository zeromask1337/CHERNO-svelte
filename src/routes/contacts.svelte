<script>
    import Article from "../components/Article.svelte";
</script>

<Article title="Контакты">
    <p>Мы будем рады ответить на Ваши вопросы.
        Наши программы могут быть адаптированы к Вашим потребностям, они могут быть использованы как самостоятельный продукт или интегрироваться с готовыми решениями.
        Возможно, Вам нужен оригинальный программный продукт для решения Ваших задач – давайте это обсудим.
        Звоните нам: +7 (495) 222- 69-51
        Пишите : office@inproekt.ru
    </p>
    <hr>
    <h3>Можете использовать форму обратной связи:</h3>

    <form action="/action_page.php">
        <label for="fname">Тема</label>
        <input type="text" id="fname" name="fname"><br><br>
        <label for="lname">От кого</label>
        <input type="text" id="lname" name="lname"><br><br>
        <label for="w3review">Текст сообщения</label>
        <textarea id="w3review" name="w3review" rows="4" cols="50"></textarea>
        <input type="submit" value="Submit">
    </form>

</Article>

<style>
    hr, h3 {
        margin: 20px 0;
    }

    input {
        margin-bottom: 10px;
    }


    form {
        max-width: 400px;

        display: flex;
        flex-flow: column;
    }
</style>