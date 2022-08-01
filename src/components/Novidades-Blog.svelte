<link href="https://fonts.googleapis.com/css2?family=Encode+Sans:wght@400;500;700&display=swap" rel="stylesheet">
<section id="novidades">
    <div class="container">
        <img class="fotobuiu" src="Imagens/image 7.svg" alt="Foto Buiu no Viela">
        <div class="informações">
            <div>
                <h4>Novidades</h4>
            </div>
            <div>
                <h2>Projeto Viela 10 anos</h2>
            </div>
            <div>
                <p>Eu participo do Projeto Viela desde 2009. Organizei o Cine Viela, ajudei o Futebol e Leitura, fiz aulas de inglês <br> e recentemente me apaixonei pelas aulas de gastronomia. Sonho com o dia em que poderei dar aula de culinária <br> para as crianças da comunidade.</p>
            </div>
            <div>
                <!-- svelte-ignore a11y-invalid-attribute -->
                <a href="#">Saiba mais</a>            
            </div>
        </div>
        <div class="linha"></div>
    </div>
</section>


<style>
#novidades{
    width: 100%;
    height: 1037px;
    background:#fff;
    font-family: 'Encode Sans';

    
}
.container{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin-top: 66px;

}
.fotobuiu{
    max-width: 1440px;
    display: flex;
    justify-self: center;

}
.informações{
    height:270px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding-right: 220px;

}
.linha{
    display: flex;
    justify-self: center;
    align-self: center;
    max-width: 1440px;
    width: 1155px;
    height: 40px;
    border-bottom: 1px solid #000000;

}
h4{
    font-size: 16px;
    font-weight: 500;
    margin-top: 10px;
    margin-bottom: 8px;
}
h2{
    font-size: 40px;
    font-weight: 700;
    margin-top: 0;
    margin-bottom: 16px;
}
p{
    font-size: 16px;
    font-weight: 400;
    margin-top: 0;
    margin-bottom: 32px;
    line-height: 24px;
}
a{
    font-size: 16px;
    font-weight: 500;
    color: #000000;
    margin-top: 0;
    width: 90px;
    text-decoration: none;
    border-bottom:1px solid #000000 ;
}

</style>