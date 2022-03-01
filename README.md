# Repositório do desafio de projeto Git/Github da Dio
Repositório criado para o desafio de projeto.

## Programação do site

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>FoodBox</title>
  </head>
  <body>
    <style>
      body {
        background: silver;
        font-family: "roboto";
      }
      .Titulo {
        background: red;
        color: white;
        padding: 15px;
        border-radius: 25px;
      }
      .Produto {
        background: white;
        padding: 10px;
        border-radius: 25px;
        margin-bottom: 10px;
        cursor: pointer;
        border: 5px solid white;      
        }

        .botao {
        background: green;
        padding: 5px;
        border-radius: 25px;
        margin-bottom: 10px;
        cursor: pointer;
        border: 5px solid white;
        color: white;
      
        }

      
      h1 {
        margin: 0;
      }
      h2 {
        margin: 0;
      }

      h3 {
        margin-top: 10px;
        font-size: 30px;
        margin-bottom: 5px;
      }
      h4 {
        margin-top: 0px;
        margin-bottom: 5px;
        font-size: 20px;

        }

        h5 {
        margin-top: 0px;
        margin-bottom: 5px;
        font-size: 30px;

        }


        img {
          width: 140px;
          border-radius: 25px;
          float: right;

        }

    </style>

  </head>
</body>

    <body>
    <div class="Titulo">
      <h1>FoodBox</h1>
      <h2>Monte seu Box e receba em 15 minutos!</h2>
    </div>

    <h3>Primeiro, seu prato</h3>

    <div id="frango" class="Produto" onclick="escolherFrango()">
        <img
        src=https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRTjb-6AR9NUutnN66g0DbMG4qFie4vVNOzng&usqp=CAU
        />
  
        <h4>Frango Yin Yang</h4>
        <p>Um pouco de batata, um pouco de salada</p>
        <p><strong>R$19,90</strong></p>
      </div>


      <div id="carne" class="Produto" onclick="escolherCarne()">
          <img
          src=https://static.clubedaanamariabraga.com.br/wp-content/uploads/2019/10/salada-de-carne-desfiada.jpg
          />
    
          <h4>Carne com Salada</h4>
          <p>Tiras de carne com salada</p>
          <p><strong>R$22,90</strong></p>
        </div>
    
        <h5>Agora, sua Bebida</h5>


        <div id="coca" class="Produto" onclick="escolherCoca()">
            <img 
            src=https://promoções2022.com/wp-content/uploads/2021/02/z18-768x405.jpg
            />
      
            <h4>Coca Cola KS</h4>
            <p>Muito mais sabor, para sua refeição</p>
            <p><strong>R$5,90</strong></p>
          </div>


          <div id="agua" class="Produto" onclick="escolherAgua()">
              <img 
              src=https://naturaldaterra.com.br/media/catalog/product/1/2/120286---7896065880106---agua-miner-minalba-sgas-1-5l.jpg?auto=webp&format=pjpg&width=960&height=1200&fit=cover
              />
        
              <h4>Água sem gás</h4>
              <p>Nada melhor que água para se hidratar</p>
              <p><strong>R$2,50</strong></p>
            </div>
  
            
        <h5>Por fim, sua sobremesa</h5>


        <div id="petitGateau" class="Produto" onclick="escolherPetitGateau()">
            <img 
            src=https://s2.glbimg.com/eEQGiBFvi9kHx5z4TCwohXVVXrE=/0x0:600x317/984x0/smart/filters:strip_icc()/i.s3.glbimg.com/v1/AUTH_e84042ef78cb4708aeebdf1c68c6cbd6/internal_photos/bs/2020/y/S/hAEF8hShupx3YgwPrDiw/petit-gateau-de-chocolate-com-sorvete.jpg
            
            />
      
            <h4>Petit Gateau</h4>
            <p>bolinho de chocolate recheado com chocolate derretido acompanhado por sorvete de creme</p>
            <p><strong>R$9,90</strong></p>
          </div>

          <div id="torta" class="Produto" onclick="escolherTortaHolandesa()">
              <img 
              src=https://www.unileverfoodsolutions.com.br/dam/global-ufs/mcos/SLA/calcmenu/recipes/BR-recipes/desserts-&-bakery/torta-holandesa/main-header.jpg       
              />
        
              <h4>Torta Holandesa</h4>
              <p>Um delicioso pedaçõ de torta</p>
              <p><strong>R$10,90</strong></p>
            </div>
  
            <div class="botao" onclick="finalizarPedido()">
                <center> Finalizar Pedido </center>

    <Script>

let prato;
let bebida;
let sobremesa;

    function escolherFrango(){
  document.getElementById("frango").style.borderColor = "green"; 
  document.getElementById("carne").style.borderColor = "white" 
  prato= "Frango";
}
 
  
function escolherCarne(){
  document.getElementById("frango").style.borderColor = "white"; 
  document.getElementById("carne").style.borderColor = "green" 
  prato= "Carne";
}


function escolherCoca(){
  document.getElementById("coca").style.borderColor = "green"; 
  document.getElementById("agua").style.borderColor = "white" 
bebida= "Coca";
}


function escolherAgua(){
  document.getElementById("agua").style.borderColor = "green"; 
  document.getElementById("coca").style.borderColor = "white" 
bebida= "Agua";
}

function escolherPetitGateau(){
  document.getElementById("petitGateau").style.borderColor = "green"; 
  document.getElementById("torta").style.borderColor = "white"
sobremesa= "Petit Gateau";
}

function escolherTortaHolandesa(){
  document.getElementById("petitGateau").style.borderColor = "white"; 
  document.getElementById("torta").style.borderColor = "green"
sobremesa= "Torta";
}


function finalizarPedido(){

  let mensagem
  mensagem =  "Olá, gostaria de pedir um combo " + prato + " ," + bebida + " e " + sobremesa + "!"
  window.open("https://wa.me/+5511999999999?text=" + mensagem );
}
    </Script>

  </body>
</html>



## Link FoodBox

[Link para fazer o pedido](https://duxp56.csb.app/)
