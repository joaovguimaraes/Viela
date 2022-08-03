<script>
    import Carousel from "svelte-carousel";

    let cards = [
        {
            index: 0,
            title: "Jiu-Jitsu",
            image: "./jiujitsu.svg",
            paragraph:
                "Em  Meados de 2009 Anderson “buiu” sentiu a necessidade de retribuir ao mundo a ajuda que recebeu a decidiu fazer na frente “de casa” um cinema para as crianças da comunidade.",
        },
        {
            index: 1,
            title: "Inglês",
            image: "./jiujitsu.svg",
            paragraph:
                "Em  Meados de 2009 Anderson “buiu” sentiu a necessidade de retribuir ao mundo a ajuda que recebeu a decidiu fazer na frente “de casa” um cinema para as crianças da comunidade.",
        },
        {
            index: 2,
            title: "Música",
            image: "./jiujitsu.svg",
            paragraph:
                "Em  Meados de 2009 Anderson “buiu” sentiu a necessidade de retribuir ao mundo a ajuda que recebeu a decidiu fazer na frente “de casa” um cinema para as crianças da comunidade.",
        },
        {
            index: 3,
            title: "Música",
            image: "./jiujitsu.svg",
            paragraph:
                "Em  Meados de 2009 Anderson “buiu” sentiu a necessidade de retribuir ao mundo a ajuda que recebeu a decidiu fazer na frente “de casa” um cinema para as crianças da comunidade.",
        },
        {
            index: 4,
            title: "Música",
            image: "./jiujitsu.svg",
            paragraph:
                "Em  Meados de 2009 Anderson “buiu” sentiu a necessidade de retribuir ao mundo a ajuda que recebeu a decidiu fazer na frente “de casa” um cinema para as crianças da comunidade.",
        },
    ];
    let carousel;
    function goToPrevPage() {
        carousel.goToPrev({ animated: true });
    }
    function goToNextPage() {
        carousel.goToNext({ animated: true });
    }
    function goToPage(index) {
        carousel.goTo(index, { animated: true });
    }
</script>

<section class="atividades">
    <div class="content">
        <h4>ATIVIDADES</h4>
        <h2>O que rola aqui</h2>
        <div class="historia">
            <p>
                Em Meados de 2009 Anderson “buiu” sentiu <br /> a necessidade de
                retribuir ao mundo a ajuda que recebeu a decidiu fazer na frente
                “de casa” um cinema para as crianças da comunidade.
            </p>
        </div>

        <img class="iconeC" src="/icoOpen.svg" alt="icone C" />

        <div class="iconeflor" id="fundoflor" />
        <div class="iconeflor" id="frenteflor" />

        <div class="iconenuvem" id="nuvem1" />
        <div class="iconenuvem" id="nuvem2" />
        <div class="iconenuvem" id="nuvem3" />

        <div class="iconeestrela" id="estrela1fundo" />
        <div class="iconeestrela" id="estrela1frente" />

        <div class="iconeestrela" id="estrela2fundo" />
        <div class="iconeestrela" id="estrela2frente" />

        <div class="iconeestrela" id="estrela3fundo" />
        <div class="iconeestrela" id="estrela3frente" />
    </div>
    <div class="carousel">
        <Carousel
            particlesToShow={3}
            bind:this={carousel}
            arrows={false}
            let:currentPageIndex
            let:pagesCount
            let:showPage
        >
            <div slot="dots" class="custom-dots">
                {#each cards as card}
                    <button
                        class="dots {card.index == currentPageIndex
                            ? 'active-dots'
                            : ''}"
                        style="margin-left: {card.index == cards.length
                            ? '0px'
                            : '16px'} ;"
                        on:click={() => goToPage(card.index)}
                    />
                {/each}
            </div>
            {#each cards as card}
                <div class="card-spacing">
                    <div class="card">
                        <div class="card-content">
                            <h4 class="card-title">{card.title}</h4>
                            <div class="icones">
                                <div id="icoPolygon">
                                    <img
                                        id="imgNoRacismo"
                                        alt="Punho"
                                        src="noRacismo.png"
                                    />
                                </div>
                            </div>

                            <img src={card.image} alt={card.title} />
                            <p class="card-paragraph">{card.paragraph}</p>
                        </div>
                    </div>
                </div>
            {/each}
        </Carousel>

        <div class="div-buttons-carousel">
            <button class="button-carousel" on:click={goToPrevPage}>
                <img src="./Arrow2.svg" alt="arrow" />
            </button>
            <button class="button-carousel" on:click={goToNextPage}>
                <img src="./Arrow1.svg" alt="arrow" />
            </button>
        </div>
    </div>
</section>

<style>
    .atividades {
        display: flex;
        flex-direction: row;
        height: 1068px;
        background: #000000;
        font-family: "Encode Sans";
        color: #ffffff;
        overflow-x: hidden;
        padding-top: 166px;
    }
    .content {
        padding-left: 142px;
        display: flex;
        flex-direction: column;
    }
    .dots {
        height: 20px;
        width: 20px;
        border: 2px solid #fff;
        border-radius: 50%;
        background-color: #000;
    }
    .custom-dots{
        align-self: flex-start;
        margin-top:25px;
    }
    .active-dots {
        background: #ffdb00;
    }
    #imgNoRacismo {
        width: 12px;
        height: 15px;
    }
    .card-title {
        color: #000;
        font-weight: bold;
        size: 16px;
        line-height: 24px;
        margin-bottom: 16px;
    }
    .card-paragraph {
        color: #000;
        size: 16px;
        line-height: 24px;
    }
    .card {
        height: 444px;
        width: 330px;
        margin-block: 32px;
        border: 2px solid #000;
        background: #ffdb00;
        box-shadow: -10px 10px #fff;
    }
    .card-content {
        margin-inline: 24px;
        margin-block: 32px;
        display: flex;
        flex-direction: column;
    }
    .card-spacing {
        position: relative;
        box-sizing: content-box;
        margin: 16px;
        left: -70px;
    }
    .icones {
        position: absolute;
        z-index: 1;
        transform: rotate(-15deg);

        align-self: flex-end;
        top: 75px;
        width: 65px;
        height: 65px;

        display: flex;
        justify-content: center;
        align-items: center;
        background-color: #fff;
        clip-path: polygon(
            100% 50%,
            74.73% 58.03%,
            90.45% 79.39%,
            65.28% 71.03%,
            65.45% 97.55%,
            50% 76%,
            34.55% 97.55%,
            34.72% 71.03%,
            9.55% 79.39%,
            25.27% 58.03%,
            0% 50%,
            25.27% 41.97%,
            9.55% 20.61%,
            34.72% 28.97%,
            34.55% 2.45%,
            50% 24%,
            65.45% 2.45%,
            65.28% 28.97%,
            90.45% 20.61%,
            74.73% 41.97%
        );
    }
    #icoPolygon {
        width: 60px;
        height: 60px;
        align-items: center;
        display: flex;
        justify-content: center;
        background-color: #000;
        clip-path: polygon(
            100% 50%,
            74.73% 58.03%,
            90.45% 79.39%,
            65.28% 71.03%,
            65.45% 97.55%,
            50% 76%,
            34.55% 97.55%,
            34.72% 71.03%,
            9.55% 79.39%,
            25.27% 58.03%,
            0% 50%,
            25.27% 41.97%,
            9.55% 20.61%,
            34.72% 28.97%,
            34.55% 2.45%,
            50% 24%,
            65.45% 2.45%,
            65.28% 28.97%,
            90.45% 20.61%,
            74.73% 41.97%
        );
    }
    h4 {
        font-size: 16px;
        font-weight: 500;
        margin: 0;
    }
    h2 {
        font-size: 40px;
        font-weight: 700;
        margin-top: 8px;
        margin-bottom: 0;
    }
    .historia {
        display: flex;
        width: 327px;
        height: 96px;
        font-size: 16px;
        font-weight: 400;
        font-style: normal;
        line-height: 150%;
        margin-top: 32px;
        margin-right: 125px;
    }
    .iconeC {
        width: 100px;
        height: 100px;
        position: absolute;
        top: 480px;
        left: 215px;
    }
    .iconeflor {
        clip-path: polygon(
            75% 50%,
            75.1342% 49.983%,
            75.5195% 49.8668%,
            76.1054% 49.5639%,
            76.8147% 49.0091%,
            77.5525% 48.1673%,
            78.2173% 47.0378%,
            78.713% 45.6543%,
            78.9605% 44.0813%,
            78.9068% 42.4063%,
            78.5317% 40.7295%,
            77.8496% 39.1524%,
            76.9084% 37.7658%,
            75.7836% 36.6386%,
            74.5694% 35.8108%,
            73.3677% 35.2877%,
            72.276% 35.0404%,
            71.376% 35.0085%,
            70.724% 35.1078%,
            70.344% 35.2402%,
            70.2254% 35.3054%,
            70.3241% 35.2128%,
            70.5674% 34.8923%,
            70.8633% 34.3028%,
            71.1111% 33.437%,
            71.2132% 32.3223%,
            71.0871% 31.0178%,
            70.675% 29.6072%,
            69.9506% 28.1892%,
            68.9226% 26.8655%,
            67.6336% 25.7295%,
            66.1548% 24.8546%,
            64.5783% 24.2859%,
            63.0058% 24.0352%,
            61.5369% 24.0791%,
            60.2572% 24.3623%,
            59.2286% 24.8039%,
            58.4818% 25.3071%,
            58.0126% 25.7707%,
            57.783% 26.1012%,
            57.7254% 26.2236%,
            57.7508% 26.0907%,
            57.7593% 25.6884%,
            57.6522% 25.0376%,
            57.3438% 24.1915%,
            56.7712% 23.2297%,
            55.9024% 22.2484%,
            54.7398% 21.3494%,
            53.3203% 20.628%,
            51.7106% 20.1614%,
            50% 20%,
            48.2894% 20.1614%,
            46.6797% 20.628%,
            45.2602% 21.3494%,
            44.0976% 22.2484%,
            43.2288% 23.2297%,
            42.6562% 24.1915%,
            42.3478% 25.0376%,
            42.2407% 25.6884%,
            42.2492% 26.0907%,
            42.2746% 26.2236%,
            42.217% 26.1012%,
            41.9874% 25.7707%,
            41.5182% 25.3071%,
            40.7714% 24.8039%,
            39.7428% 24.3623%,
            38.4631% 24.0791%,
            36.9942% 24.0352%,
            35.4217% 24.2859%,
            33.8452% 24.8546%,
            32.3664% 25.7295%,
            31.0774% 26.8655%,
            30.0494% 28.1892%,
            29.325% 29.6072%,
            28.9129% 31.0178%,
            28.7868% 32.3223%,
            28.8889% 33.437%,
            29.1367% 34.3028%,
            29.4326% 34.8923%,
            29.6759% 35.2128%,
            29.7746% 35.3054%,
            29.656% 35.2402%,
            29.276% 35.1078%,
            28.624% 35.0085%,
            27.724% 35.0404%,
            26.6323% 35.2877%,
            25.4306% 35.8108%,
            24.2164% 36.6386%,
            23.0916% 37.7658%,
            22.1504% 39.1524%,
            21.4683% 40.7295%,
            21.0932% 42.4063%,
            21.0395% 44.0813%,
            21.287% 45.6543%,
            21.7827% 47.0378%,
            22.4475% 48.1673%,
            23.1853% 49.0091%,
            23.8947% 49.5639%,
            24.4805% 49.8668%,
            24.8658% 49.983%,
            25% 50%,
            24.8658% 50.017%,
            24.4805% 50.1332%,
            23.8947% 50.4361%,
            23.1853% 50.9909%,
            22.4475% 51.8327%,
            21.7827% 52.9622%,
            21.287% 54.3457%,
            21.0395% 55.9187%,
            21.0932% 57.5937%,
            21.4683% 59.2705%,
            22.1504% 60.8476%,
            23.0916% 62.2342%,
            24.2164% 63.3614%,
            25.4306% 64.1892%,
            26.6323% 64.7123%,
            27.724% 64.9596%,
            28.624% 64.9915%,
            29.276% 64.8922%,
            29.656% 64.7598%,
            29.7746% 64.6946%,
            29.6759% 64.7873%,
            29.4326% 65.1077%,
            29.1367% 65.6972%,
            28.8889% 66.563%,
            28.7868% 67.6777%,
            28.9129% 68.9822%,
            29.325% 70.3928%,
            30.0494% 71.8108%,
            31.0774% 73.1345%,
            32.3664% 74.2705%,
            33.8452% 75.1455%,
            35.4217% 75.7141%,
            36.9942% 75.9648%,
            38.4631% 75.9209%,
            39.7428% 75.6377%,
            40.7714% 75.1961%,
            41.5182% 74.6929%,
            41.9874% 74.2293%,
            42.217% 73.8988%,
            42.2746% 73.7764%,
            42.2492% 73.9093%,
            42.2407% 74.3116%,
            42.3478% 74.9624%,
            42.6562% 75.8085%,
            43.2288% 76.7703%,
            44.0976% 77.7516%,
            45.2602% 78.6506%,
            46.6797% 79.372%,
            48.2894% 79.8386%,
            50% 80%,
            51.7106% 79.8386%,
            53.3203% 79.372%,
            54.7398% 78.6506%,
            55.9024% 77.7516%,
            56.7712% 76.7703%,
            57.3438% 75.8085%,
            57.6522% 74.9624%,
            57.7593% 74.3116%,
            57.7508% 73.9093%,
            57.7254% 73.7764%,
            57.783% 73.8988%,
            58.0126% 74.2293%,
            58.4818% 74.6929%,
            59.2286% 75.1961%,
            60.2572% 75.6377%,
            61.5369% 75.9209%,
            63.0058% 75.9648%,
            64.5783% 75.7141%,
            66.1548% 75.1455%,
            67.6336% 74.2705%,
            68.9226% 73.1345%,
            69.9506% 71.8108%,
            70.675% 70.3928%,
            71.0871% 68.9822%,
            71.2132% 67.6777%,
            71.1111% 66.563%,
            70.8633% 65.6972%,
            70.5674% 65.1077%,
            70.3241% 64.7873%,
            70.2254% 64.6946%,
            70.344% 64.7598%,
            70.724% 64.8922%,
            71.376% 64.9915%,
            72.276% 64.9596%,
            73.3677% 64.7123%,
            74.5694% 64.1892%,
            75.7836% 63.3614%,
            76.9084% 62.2342%,
            77.8496% 60.8476%,
            78.5317% 59.2705%,
            78.9068% 57.5937%,
            78.9605% 55.9187%,
            78.713% 54.3457%,
            78.2173% 52.9622%,
            77.5525% 51.8327%,
            76.8147% 50.9909%,
            76.1054% 50.4361%,
            75.5195% 50.1332%,
            75.1342% 50.017%
        );
    }
    #fundoflor {
        background: #ffffff;
        width: 288px;
        height: 290px;
        position: relative;
        left: 45px;
        top: 108px;
    }
    #frenteflor {
        background: #000000;
        width: 282px;
        height: 286px;
        position: relative;
        left: 48px;
        top: -180px;
    }
    .carousel {
        width: 1000px;
    }
    .button-carousel {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 50px;
        width: 50px;
        border: 2px #fff solid;
        background: #ffdb00;
        border-radius: 50%;
    }

    .div-buttons-carousel {
        width: 47vw;
        position: relative;
        top: -85px;
        display: flex;
        flex-direction: row;
        justify-content: flex-end;
        margin-top: 42px;
        gap: 24px;
    }

    .iconenuvem {
        width: 45px;
        height: 45px;
        background: #ffffff;
        border-radius: 50%;
        position: absolute;
    }
    #nuvem1 {
        left: 275px;
        top: 670px;
    }
    #nuvem2 {
        left: 243px;
        top: 677px;
    }
    #nuvem3 {
        left: 211px;
        top: 684px;
    }
    .iconeestrela {
        clip-path: polygon(
            75.2736% 50%,
            75.3253% 49.4695%,
            75.4798% 48.9321%,
            75.7351% 48.3809%,
            76.0876% 47.8094%,
            76.5309% 47.2115%,
            77.0558% 46.5821%,
            77.6499% 45.917%,
            78.2983% 45.2137%,
            78.9851% 44.4708%,
            79.6951% 43.6881%,
            80.4157% 42.8661%,
            81.1383% 42.0051%,
            81.8582% 41.105%,
            82.5741% 40.1653%,
            83.287% 39.1844%,
            83.9989% 38.1603%,
            84.7124% 37.0906%,
            85.4289% 35.9727%,
            86.1474% 34.8051%,
            86.8627% 33.5877%,
            87.5634% 32.324%,
            88.2313% 31.0218%,
            88.8412% 29.6943%,
            89.3636% 28.3597%,
            89.7676% 27.0402%,
            90.0247% 25.7602%,
            90.111% 24.5448%,
            90.0095% 23.4177%,
            89.7108% 22.4003%,
            89.2127% 21.5103%,
            88.5202% 20.7616%,
            87.6449% 20.1631%,
            86.6043% 19.7183%,
            85.4217% 19.4248%,
            84.125% 19.2737%,
            82.7452% 19.2502%,
            81.3144% 19.3347%,
            79.8634% 19.5045%,
            78.4186% 19.7372%,
            77.0002% 20.0132%,
            75.6214% 20.3173%,
            74.2889% 20.6398%,
            73.0043% 20.9758%,
            71.7665% 21.3237%,
            70.5725% 21.6844%,
            69.4193% 22.0593%,
            68.3043% 22.4497%,
            67.2259% 22.8563%,
            66.1837% 23.2775%,
            65.1792% 23.7088%,
            64.2155% 24.1421%,
            63.2967% 24.5657%,
            62.4274% 24.9651%,
            61.6113% 25.3246%,
            60.8505% 25.6293%,
            60.1449% 25.8662%,
            59.4925% 26.0248%,
            58.8893% 26.0973%,
            58.3305% 26.0782%,
            57.81% 25.9634%,
            57.3214% 25.7503%,
            56.858% 25.4373%,
            56.4127% 25.0241%,
            55.9781% 24.5123%,
            55.5465% 23.906%,
            55.11% 23.2122%,
            54.6611% 22.4417%,
            54.1926% 21.6076%,
            53.6983% 20.7249%,
            53.1733% 19.8079%,
            52.6142% 18.8685%,
            52.0186% 17.9152%,
            51.3851% 16.9524%,
            50.7126% 15.9811%,
            50% 15%,
            49.246% 14.0064%,
            48.4491% 12.9973%,
            47.6074% 11.9705%,
            46.7189% 10.9263%,
            45.7822% 9.86985%,
            44.7969% 8.81286%,
            43.7648% 7.77531%,
            42.6907% 6.78505%,
            41.5829% 5.87581%,
            40.4528% 5.08376%,
            39.3149% 4.44377%,
            38.1856% 3.98612%,
            37.0824% 3.73431%,
            36.0224% 3.704%,
            35.0221% 3.90269%,
            34.096% 4.32993%,
            33.2563% 4.97749%,
            32.5117% 5.82969%,
            31.8672% 6.86368%,
            31.3228% 8.05027%,
            30.8741% 9.35531%,
            30.5122% 10.7421%,
            30.2253% 12.1746%,
            30.0002% 13.6206%,
            29.8244% 15.0548%,
            29.6875% 16.4602%,
            29.5825% 17.8271%,
            29.505% 19.1526%,
            29.4535% 20.4374%,
            29.4275% 21.6844%,
            29.4277% 22.897%,
            29.4545% 24.078%,
            29.5079% 25.2293%,
            29.5864% 26.3507%,
            29.6862% 27.4393%,
            29.8005% 28.4898%,
            29.9195% 29.4945%,
            30.0307% 30.4446%,
            30.1204% 31.3319%,
            30.1751% 32.1496%,
            30.1823% 32.8939%,
            30.1315% 33.5634%,
            30.0141% 34.1594%,
            29.8232% 34.685%,
            29.5532% 35.1446%,
            29.1996% 35.5434%,
            28.7587% 35.8873%,
            28.2282% 36.1832%,
            27.6071% 36.4384%,
            26.897% 36.6615%,
            26.1024% 36.8622%,
            25.2309% 37.051%,
            24.2929% 37.2389%,
            23.3006% 37.4362%,
            22.2662% 37.6521%,
            21.2% 37.8936%,
            20.1093% 38.1654%,
            18.9978% 38.4704%,
            17.8663% 38.8099%,
            16.713% 39.1844%,
            15.5351% 39.5944%,
            14.3291% 40.0405%,
            13.0924% 40.5237%,
            11.8248% 41.0461%,
            10.5306% 41.6105%,
            9.22085% 42.221%,
            7.91515% 42.8819%,
            6.64146% 43.5974%,
            5.43436% 44.3701%,
            4.33186% 45.2001%,
            3.37157% 46.0845%,
            2.58736% 47.0171%,
            2.00696% 47.9885%,
            1.65057% 48.9872%,
            1.53042% 50%,
            1.65057% 51.0128%,
            2.00696% 52.0115%,
            2.58736% 52.983%,
            3.37157% 53.9155%,
            4.33186% 54.7999%,
            5.43436% 55.63%,
            6.64146% 56.4026%,
            7.91515% 57.1181%,
            9.22085% 57.779%,
            10.5306% 58.3895%,
            11.8248% 58.9539%,
            13.0924% 59.4763%,
            14.3291% 59.9595%,
            15.5351% 60.4056%,
            16.713% 60.8156%,
            17.8663% 61.1901%,
            18.9978% 61.5296%,
            20.1093% 61.8346%,
            21.2% 62.1064%,
            22.2662% 62.3479%,
            23.3006% 62.5638%,
            24.2929% 62.7611%,
            25.2309% 62.949%,
            26.1024% 63.1378%,
            26.897% 63.3385%,
            27.6071% 63.5616%,
            28.2282% 63.8168%,
            28.7587% 64.1127%,
            29.1996% 64.4567%,
            29.5532% 64.8554%,
            29.8232% 65.315%,
            30.0141% 65.8406%,
            30.1315% 66.4366%,
            30.1823% 67.1062%,
            30.1751% 67.8504%,
            30.1204% 68.6681%,
            30.0307% 69.5554%,
            29.9195% 70.5055%,
            29.8005% 71.5102%,
            29.6862% 72.5607%,
            29.5864% 73.6493%,
            29.5079% 74.7707%,
            29.4545% 75.922%,
            29.4277% 77.103%,
            29.4275% 78.3156%,
            29.4535% 79.5626%,
            29.505% 80.8474%,
            29.5825% 82.1729%,
            29.6875% 83.5399%,
            29.8244% 84.9452%,
            30.0002% 86.3794%,
            30.2253% 87.8255%,
            30.5122% 89.2579%,
            30.8741% 90.6447%,
            31.3228% 91.9497%,
            31.8672% 93.1363%,
            32.5117% 94.1703%,
            33.2563% 95.0225%,
            34.096% 95.6701%,
            35.0221% 96.0973%,
            36.0224% 96.296%,
            37.0824% 96.2657%,
            38.1856% 96.0139%,
            39.3149% 95.5562%,
            40.4528% 94.9162%,
            41.5829% 94.1242%,
            42.6907% 93.215%,
            43.7648% 92.2247%,
            44.7969% 91.1871%,
            45.7822% 90.1302%,
            46.7189% 89.0737%,
            47.6074% 88.0295%,
            48.4491% 87.0027%,
            49.246% 85.9936%,
            50% 85%,
            50.7126% 84.0189%,
            51.3851% 83.0476%,
            52.0186% 82.0848%,
            52.6142% 81.1315%,
            53.1733% 80.1922%,
            53.6983% 79.2751%,
            54.1926% 78.3924%,
            54.6611% 77.5583%,
            55.11% 76.7878%,
            55.5465% 76.0941%,
            55.9781% 75.4877%,
            56.4127% 74.9759%,
            56.858% 74.5627%,
            57.3214% 74.2497%,
            57.81% 74.0366%,
            58.3305% 73.9218%,
            58.8893% 73.9027%,
            59.4925% 73.9752%,
            60.1449% 74.1338%,
            60.8505% 74.3707%,
            61.6113% 74.6754%,
            62.4274% 75.0349%,
            63.2967% 75.4343%,
            64.2155% 75.8579%,
            65.1792% 76.2912%,
            66.1837% 76.7225%,
            67.2259% 77.1437%,
            68.3043% 77.5503%,
            69.4193% 77.9407%,
            70.5725% 78.3156%,
            71.7665% 78.6763%,
            73.0043% 79.0242%,
            74.2889% 79.3602%,
            75.6214% 79.6827%,
            77.0002% 79.9868%,
            78.4186% 80.2628%,
            79.8634% 80.4955%,
            81.3144% 80.6654%,
            82.7452% 80.7498%,
            84.125% 80.7263%,
            85.4217% 80.5752%,
            86.6043% 80.2817%,
            87.6449% 79.8369%,
            88.5202% 79.2384%,
            89.2127% 78.4897%,
            89.7108% 77.5997%,
            90.0095% 76.5823%,
            90.111% 75.4552%,
            90.0247% 74.2398%,
            89.7676% 72.9599%,
            89.3636% 71.6403%,
            88.8412% 70.3057%,
            88.2313% 68.9782%,
            87.5634% 67.676%,
            86.8627% 66.4123%,
            86.1474% 65.195%,
            85.4289% 64.0273%,
            84.7124% 62.9094%,
            83.9989% 61.8397%,
            83.287% 60.8156%,
            82.5741% 59.8347%,
            81.8582% 58.895%,
            81.1383% 57.995%,
            80.4157% 57.1339%,
            79.6951% 56.3119%,
            78.9851% 55.5292%,
            78.2983% 54.7863%,
            77.6499% 54.083%,
            77.0558% 53.4179%,
            76.5309% 52.7885%,
            76.0876% 52.1906%,
            75.7351% 51.6191%,
            75.4798% 51.0679%,
            75.3253% 50.5305%
        );
    }
    #estrela1fundo {
        background: #ffffff;
        width: 71px;
        height: 71px;
        position: relative;
        transform: rotate(19deg);
        left: 236px;
        top: -438px;
    }
    #estrela1frente {
        background: #000000;
        width: 67px;
        height: 67px;
        position: relative;
        transform: rotate(19deg);
        left: 238px;
        top: -507px;
    }
    #estrela2fundo {
        background: #ffffff;
        width: 71px;
        height: 71px;
        position: relative;
        transform: rotate(19deg);
        left: 265px;
        top: -400px;
    }
    #estrela2frente {
        background: #000000;
        width: 67px;
        height: 67px;
        position: relative;
        transform: rotate(19deg);
        left: 267px;
        top: -469px;
    }
    #estrela3fundo {
        background: #ffffff;
        width: 71px;
        height: 71px;
        position: absolute;
        transform: rotate(19deg);
        left: 150px;
        top: 580px;
    }
    #estrela3frente {
        background: #000000;
        width: 67px;
        height: 67px;
        position: absolute;
        transform: rotate(19deg);
        left: 152px;
        top: 582px;
    }
</style>
