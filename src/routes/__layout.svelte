<script>
    import Header from "../components/Header.svelte"
    import Footer from "../components/Footer.svelte"
    import Aside from "../components/Aside.svelte";
</script>

<Header/>
<main>
    <slot></slot>
    <Aside/>
</main>
<Footer/>

<style lang="scss">
    @import "../base";

    main {
        min-height: 90vh;

        display: flex;
        flex-flow: column;
        //align-items: center;
    }

    @media (min-width: $ipad) {
        main {
          flex-flow: row;
        }
    }
</style>