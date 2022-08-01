

<footer>

    <section class="footer">

        <div class="logoButton">
            <div id="iconeFlor">
                <!-- svelte-ignore a11y-missing-attribute -->
                <img id="logoFooter" src="footerLogo.svg">
            </div>
            <button>Seja um doador</button>
        </div>

        <div class="opções">
            <div id="contato">
                <h2>Seja um parceiro viela?</h2>
                <a class="linkFooter" href="#">projeto.viela@gmail.com</a>
            </div> 
            <h2>Navege</h2>
            <ul class="footerList">
                <li><a class="linkFooter" href="#">Blog</a></li>
                <li><a class="linkFooter" href="#">Sobre</a></li>
                <li><a class="linkFooter" href="#">Atividades</a></li>
            </ul>
        </div>

        <div class="redesSociais">
            <h2>Redes sociais:</h2>
            <ul id="redesSociais">
                <li id="liFooter"><a class="linkFooter" href="#">Instagram</a></li>
                <li id="liFooter"><a class="linkFooter" href="#">Facebook</a></li>
            </ul>
            <p id="copy">Viela 2022 - Todos os direitos reservados</p>
        </div>

    </section>

</footer>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Encode+Sans:wght@400;500;700&display=swap');
    
    footer{
        display: flex;
        justify-content: center;
        width: 100%;
        background-color: #000;
    }
    .footer {
        max-width: 1440px;
        height: 307px;
        background-color: #000;
        color: #FFFFFF;
        display: flex;
        flex-direction: row;
        box-sizing: border-box;
        align-items: center;
    }

    .logoButton {
        width: 450px;
        display: flex;
        flex-direction: row;
        height: 307px;
        padding: 60px 0px 70px 30px;
        box-sizing: border-box;
    }
    #iconeFlor {
        justify-self: center;
        display: flex;
        align-items: center;
        justify-content: center;
        width: 185px;
        height: 175px;
        background-color: #FFF;
        clip-path: polygon(90% 50%, 90.2148% 49.9729%, 90.8311% 49.7869%, 91.7686% 49.3022%, 92.9035% 48.4145%, 94.084% 47.0676%, 95.1477% 45.2604%, 95.9408% 43.0469%, 96.3368% 40.5301%, 96.2509% 37.85%, 95.6507% 35.1672%, 94.5594% 32.6439%, 93.0535% 30.4252%, 91.2538% 28.6218%, 89.3111% 27.2973%, 87.3883% 26.4604%, 85.6416% 26.0646%, 84.2016% 26.0136%, 83.1583% 26.1725%, 82.5504% 26.3843%, 82.3607% 26.4886%, 82.5185% 26.3404%, 82.9078% 25.8277%, 83.3813% 24.8845%, 83.7777% 23.4992%, 83.9411% 21.7157%, 83.7394% 19.6285%, 83.08% 17.3715%, 81.921% 15.1027%, 80.2762% 12.9848%, 78.2137% 11.1672%, 75.8476% 9.76728%, 73.3252% 8.85746%, 70.8092% 8.45633%, 68.459% 8.52663%, 66.4116% 8.97975%, 64.7658% 9.68628%, 63.5708% 10.4914%, 62.8202% 11.2331%, 62.4528% 11.7619%, 62.3607% 11.9577%, 62.4013% 11.7451%, 62.4149% 11.1014%, 62.2435% 10.0601%, 61.75% 8.70638%, 60.8339% 7.16745%, 59.4438% 5.59743%, 57.5837% 4.15911%, 55.3125% 3.00477%, 52.737% 2.25819%, 50% 2%, 47.263% 2.25819%, 44.6875% 3.00477%, 42.4163% 4.15911%, 40.5562% 5.59743%, 39.1661% 7.16745%, 38.25% 8.70638%, 37.7565% 10.0601%, 37.5851% 11.1014%, 37.5987% 11.7451%, 37.6393% 11.9577%, 37.5472% 11.7619%, 37.1798% 11.2331%, 36.4292% 10.4914%, 35.2342% 9.68628%, 33.5884% 8.97975%, 31.541% 8.52663%, 29.1908% 8.45633%, 26.6748% 8.85746%, 24.1524% 9.76728%, 21.7863% 11.1672%, 19.7238% 12.9848%, 18.079% 15.1027%, 16.92% 17.3715%, 16.2606% 19.6285%, 16.0589% 21.7157%, 16.2223% 23.4992%, 16.6187% 24.8845%, 17.0922% 25.8277%, 17.4815% 26.3404%, 17.6393% 26.4886%, 17.4496% 26.3843%, 16.8417% 26.1725%, 15.7984% 26.0136%, 14.3584% 26.0646%, 12.6117% 26.4604%, 10.6889% 27.2973%, 8.74622% 28.6218%, 6.94653% 30.4252%, 5.44063% 32.6439%, 4.34929% 35.1672%, 3.74905% 37.85%, 3.66323% 40.5301%, 4.05922% 43.0469%, 4.85235% 45.2604%, 5.91598% 47.0676%, 7.09648% 48.4145%, 8.23144% 49.3022%, 9.16888% 49.7869%, 9.78523% 49.9729%, 10% 50%, 9.78523% 50.0271%, 9.16888% 50.2131%, 8.23144% 50.6978%, 7.09648% 51.5855%, 5.91598% 52.9324%, 4.85235% 54.7396%, 4.05922% 56.9531%, 3.66323% 59.4699%, 3.74905% 62.15%, 4.34929% 64.8328%, 5.44063% 67.3561%, 6.94653% 69.5748%, 8.74622% 71.3782%, 10.6889% 72.7028%, 12.6117% 73.5396%, 14.3584% 73.9353%, 15.7984% 73.9864%, 16.8417% 73.8275%, 17.4496% 73.6157%, 17.6393% 73.5114%, 17.4815% 73.6596%, 17.0922% 74.1723%, 16.6187% 75.1155%, 16.2223% 76.5008%, 16.0589% 78.2843%, 16.2606% 80.3715%, 16.92% 82.6285%, 18.079% 84.8973%, 19.7238% 87.0152%, 21.7863% 88.8328%, 24.1524% 90.2327%, 26.6748% 91.1425%, 29.1908% 91.5437%, 31.541% 91.4734%, 33.5884% 91.0202%, 35.2342% 90.3137%, 36.4292% 89.5086%, 37.1798% 88.7669%, 37.5472% 88.2381%, 37.6393% 88.0423%, 37.5987% 88.2549%, 37.5851% 88.8986%, 37.7565% 89.9399%, 38.25% 91.2936%, 39.1661% 92.8326%, 40.5562% 94.4026%, 42.4163% 95.8409%, 44.6875% 96.9952%, 47.263% 97.7418%, 50% 98%, 52.737% 97.7418%, 55.3125% 96.9952%, 57.5837% 95.8409%, 59.4438% 94.4026%, 60.8339% 92.8326%, 61.75% 91.2936%, 62.2435% 89.9399%, 62.4149% 88.8986%, 62.4013% 88.2549%, 62.3607% 88.0423%, 62.4528% 88.2381%, 62.8202% 88.7669%, 63.5708% 89.5086%, 64.7658% 90.3137%, 66.4116% 91.0202%, 68.459% 91.4734%, 70.8092% 91.5437%, 73.3252% 91.1425%, 75.8476% 90.2327%, 78.2137% 88.8328%, 80.2762% 87.0152%, 81.921% 84.8973%, 83.08% 82.6285%, 83.7394% 80.3715%, 83.9411% 78.2843%, 83.7777% 76.5008%, 83.3813% 75.1155%, 82.9078% 74.1723%, 82.5185% 73.6596%, 82.3607% 73.5114%, 82.5504% 73.6157%, 83.1583% 73.8275%, 84.2016% 73.9864%, 85.6416% 73.9353%, 87.3883% 73.5396%, 89.3111% 72.7028%, 91.2538% 71.3782%, 93.0535% 69.5748%, 94.5594% 67.3561%, 95.6507% 64.8328%, 96.2509% 62.15%, 96.3368% 59.4699%, 95.9408% 56.9531%, 95.1477% 54.7396%, 94.084% 52.9324%, 92.9035% 51.5855%, 91.7686% 50.6978%, 90.8311% 50.2131%, 90.2148% 50.0271%);
    }
    #logoFooter {
       max-width: 114px;
       max-height: 79px;
       padding: 0px 0px 10px 5px;
    }
    button {
        background: #FFDB00;
        border: 1px solid #FFFFFF;
        border-radius: 60px;
        color: #000;
        font-family:'Encode Sans';
        font-weight: 700;
        font-size: 16px;
        line-height: 20px;
        width: 200px;
        height: 52px;
        align-self: flex-end;
        position: relative;
        right: 70px;
        bottom: -10px;
    }
    .opções {
        width: 450px;
        display: flex;
        flex-direction: column;
        font-family: 'Encode Sans';
        font-weight: 400;
        height: 200px;
    }
    .redesSociais {
        display: flex;
        flex-direction: column;
        font-family: 'Encode Sans';
        height: 200px;
    }
    .footerList{
        display: flex;
        flex-direction: row;
        margin: 0%;
    }

    ul {
        padding: 0%;
        list-style: none;
    }

    .linkFooter {
        padding-right: 32px;
        color: #FFF;
        list-style: none;
        text-decoration: underline;
        text-decoration-style: solid;
        text-underline-offset: 0.4rem;
        font-size: 16px;
    }
    h2 {
        margin: 0%;
        padding-bottom: 16px;
        font-weight: 700;
        font-size: 24px;
    }
    #contato {
        padding-bottom: 36px;
    }

    #redesSociais {
        margin: 0%;
        display: flex;
        flex-direction: column;
    }
    #liFooter {
        padding-bottom:20px ;
    }
    #copy {
    padding-top: 15px;
}

</style>