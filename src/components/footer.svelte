<footer class="viela">
    <link href="https://fonts.googleapis.com/css2?family=Encode+Sans:wght@400;500;700&display=swap" rel="stylesheet">
    <div class="footer1">
        <img class="iconefooter" src="/Icone Group 2.png" alt="Icone">
        <img class="logofooter" src="/Logo.png" alt="Logo">
        <p class="doador">Seja um doador</p>
    </div>
    <div class="footer2e3">
        <div class="footer2">
            <div>
                <h3 class="footerh3">Seja um parceiro viela?</h3>
                <a class="footerlinks" href="mailto:projeto.viela@gmail.com"> projeto.viela@gmail.com</a>
            </div>
            <div class="footer2lista">
                <h3>Navegue</h3>
                <a class="footerlinks" href="#">Blog</a>
                <a class="footerlinks" href="#">Sobre</a>
                <a class="footerlinks" href="#">Atividades</a>
            </div>
        </div>
        <div class="footer3">
            <h3 class="footerh3">Redes sociais</h3>
            <div class="footer3lista">
                <li id="liFooter"><a class="footerlinks" href="#">Instagran</a></li>
                <li id="liFooter"><a class="footerlinks" href="#">Facebook</a>
                </li>
                <p>Viela 2022 - Todos os direitos reservados</p>
            </div>
        </div>
    </div>

    

</footer>

<style>
    .viela{
        max-width: 1440px;
        height: 307px;
        margin:15%;
        position: absolute;
        display: flex;
        flex-direction: row;
        left: 0px;
        top: 2000px;
        background-color: #000;
        color: #fff;
       
       
    }
    .footer1{
        width: 564px;
        height: 307px;

    }
    
    .iconefooter{
        position:absolute;
        top: 30px ;
        left: 118px;

    }
    .logofooter{
        position:absolute;
        top: 125px;
        left: 190px;
        border-radius: 21px;
    }
    .doador{
        position: absolute;
        width: 119px;
        height: 15px;
        left: 267px;
        top: 173px;
        background-color: #ffdb00;
        border: 1px solid #FFFFFF;
        border-radius: 60px;
        padding: 16px 40px;
        color: #000;
        font-family: 'Encode Sans';
        font-weight: 700;
        font-size: 16px;
    }

    .footer2e3{
        display: flex;
        flex-direction: row;
        width: 734px;
        height: 172px;
        margin:61px 142px 78px 564px;
        margin-block:61px 142px 78px 564px ;
    }
    .footer2{
        flex-direction: column;
        width: 448px;
        height: 172px;
        font-family: 'Encode Sans';
        font-weight: 400;
    }
    .footer2a{
        line-height: 1px;
    }
    .footerh3{
        font-family: 'Encode Sans';
        font-style: normal;
        font-weight: 700;
        font-size: 24px;
    }
    .footer2lista{
        word-spacing: 32px;
    }
    .footerlinks{
        color: #ffffff;
        font-weight: 400;
        font-size: 16px;
        font-style: normal;
        text-decoration:none;
        border-bottom: 1px solid #FFFFFF;
        padding-bottom: 4px;
    }
    .footer3{
        width: 330px;
        height: 172px;
        font-family: 'Encode Sans';
        font-weight: 400;
    }
    #liFooter{
        padding-bottom: 15px;
        list-style-type: none;


}


</style>