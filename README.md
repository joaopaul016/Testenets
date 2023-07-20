<!DOCTYPE html>
<html>
<head>
  <title>Colinhas 3P</title>
  <style>
    body {
     background-color: #78c6f0;
      text-align: center;
      padding-top: 100px;
      font-family: Arial, Helvetica, sans-serif;
      font-weight: lighter;
      font-size: 20px;
    }
    .Formulario {
      background-image: url(https://cloudinary.com/blog/wp-content/uploads/sites/12/2022/02/Mario_1.gif); 
      border-radius: 100px;
      cursor: pointer;
      position: center;
      font-weight: bolder;
}

    .tramitardespacho {
      background-color: rgb(197, 14, 14);
      color: white;
      padding: 50px 99px;
      font-size: 50px;
      font-weight: bolder;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      position: fixed;
      top: 20px;
      left: 5px; 
    }

    .clienteatendido {
      background-color: rgb(74, 180, 13);
      color: white;
      padding: 50px 70px;
      font-size: 50px;
      font-weight: bolder;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      position: fixed;
      top: 190px;
      left: 5px; 
    }

    .romaneio {
      background-color: rgb(255, 136, 0);
      color: white;
      padding: 50px 43px;
      font-size: 50px;
      font-weight: bolder;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      position: fixed;
      top: 358px;
      left: 5px; 
    }

    .hidden {
      display: none;
    }
  </style>
</head>
<body>
  <div class="Formulario" id="welcome">
    <h1>Bem-vindo(a) à Colinhas Nets!</h1>
    <p>Insira seu nome:</p>
    <input type="text" id="nameInput">
    <br><br>
    <button onclick="showCancelPage()">Prosseguir</button>
    <img src="https://logodownload.org/wp-content/uploads/2014/06/magalu-logo-1.png" width="100" style="right: 10px; top: 590px; position: absolute">
    <img src="https://i.gifer.com/origin/34/34338d26023e5515f6cc8969aa027bca.gif" width= 20px; style="left: 670px; top: 350px; position: absolute">
  </div>
  
  <div id="cancelPage" class="hidden">
    <button class="tramitardespacho" onclick="copyCancellation()">Acionar seller</button>
    <button class="clienteatendido" onclick="copyPostagem()">Cliente Atendido</button>
    <button class="romaneio" onclick="ccopyromaneio()">Solicitar Romaneio</button>
    <img src="https://logodownload.org/wp-content/uploads/2014/06/magalu-logo-1.png" width="100" style="right: 10px; top: 590px; position: absolute">
  </div>
  
  <script>
    function showCancelPage() {
      var welcomeDiv = document.getElementById("welcome");
      var cancelPageDiv = document.getElementById("cancelPage");
      var name = document.getElementById("nameInput").value;
      
      welcomeDiv.classList.add("hidden");
      cancelPageDiv.classList.remove("hidden");
      
      var currentDate = new Date();
      var daysToAdd = 2; 

 var currentDate = new Date();
      var daysToAdd = 2; }

        
      function copyCancellation() {
      var name = document.getElementById("nameInput").value;
      var currentDate = new Date();
      var daysToAdd = 2; // Número de dias úteis a serem adicionados
      
      // Adiciona os dias úteis à data atual
      while (daysToAdd > 0) {
        currentDate.setDate(currentDate.getDate() + 1);
        var dayOfWeek = currentDate.getDay();
        if (dayOfWeek !== 0 && dayOfWeek !== 6) {
          daysToAdd--;
        }
      }
      // Adiciona os dias úteis à data atual
      while (daysToAdd > 0) {
        currentDate.setDate(currentDate.getDate() + 1);
        var dayOfWeek = currentDate.getDay();
        if (dayOfWeek !== 0 && dayOfWeek !== 6) {
          daysToAdd--;
        }
      }
      
       // Adiciona os dias úteis à data atual
       while (daysToAdd > 0) {
        currentDate.setDate(currentDate.getDate() + 2);
        var dayOfWeek = currentDate.getDay();
        if (dayOfWeek !== 0 && dayOfWeek !== 6) {
          daysToAdd--;
        }
      }

      var formattedDate = currentDate.toLocaleDateString("pt-BR");
      
      var message = "Olá, Lojista. \n\n" +
                    "Tudo bem?.\n\n" +
                    "Por favor, despachar o pedido e informar o rastreamento atualizado.\n\n" +
                    "Na impossibilidade do envio, realize o check-in no portal.\n\n" +
                    name + "\n" +
                    "Backoffice Netshoes";
      
                    navigator.clipboard.writeText(message)
        .then(function() {
          ;
        })
        .catch(function(error) {
          console.error("Erro ao copiar a mensagem: ", error);
        });
    }
    
    function copyPostagem() {
      var name = document.getElementById("nameInput").value;
      var currentDate = new Date();
      var daysToAdd = 2; // Número de dias úteis a serem adicionados
      
      // Adiciona os dias úteis à data atual
      while (daysToAdd > 0) {
        currentDate.setDate(currentDate.getDate() + 1);
        var dayOfWeek = currentDate.getDay();
        if (dayOfWeek !== 0 && dayOfWeek !== 6) {
          daysToAdd--;
        }
      }
      
      var formattedDate = currentDate.toLocaleDateString("pt-BR");
      
      var message = "Devido à falta de cumprimento do SLA do Lojista, cliente atendido com a devolução de valores/vale-compra." +
                    " Se precisar de ajuda novamente, pode me chamar por aqui! \n\n"+
                    name + "\n" +
                    "Backoffice Netshoes";
      // Copia a mensagem para a área de transferência
      navigator.clipboard.writeText(message)
        .then(function() {
          ;
        })
        .catch(function(error) {
          console.error("Erro ao copiar a mensagem: ", error);
        });
    }
    function ccopyromaneio() {
      var name = document.getElementById("nameInput").value;
      var currentDate = new Date();
      var daysToAdd = 2; // Número de dias úteis a serem adicionados
      
      // Adiciona os dias úteis à data atual
      while (daysToAdd > 0) {
        currentDate.setDate(currentDate.getDate() + 1);
        var dayOfWeek = currentDate.getDay();
        if (dayOfWeek !== 0 && dayOfWeek !== 6) {
          daysToAdd--;
        }
      }
      
      var formattedDate = currentDate.toLocaleDateString("pt-BR");
      
      var message = "Olá, Lojista! Tudo bem? \n\n" +
                    "Por gentileza realizar o despacho do produto e informar o rastreamento atualizado. Caso já tenha realizado o despacho, nos retornar com o romaneio." +
                    " Já estamos dando andamento em sua solicitação de cancelamento.\n\n" +
                    "Na impossibilidade do envio, realize o check-in no portal..\n\n" +
                    name + "\n" +
                    "Atenciosamente,Backoffice Netshoes";
      
      // Copia a mensagem para a área de transferência
      navigator.clipboard.writeText(message)
        .then(function() {
          ;
        })
        .catch(function(error) {
          console.error("Erro ao copiar a mensagem: ", error);
        });
    }

    function ccopyCancellation2() {
      var name = document.getElementById("nameInput").value;
      var currentDate = new Date();
      var daysToAdd = 2; // Número de dias úteis a serem adicionados
      
      // Adiciona os dias úteis à data atual
      while (daysToAdd > 0) {
        currentDate.setDate(currentDate.getDate() + 1);
        var dayOfWeek = currentDate.getDay();
        if (dayOfWeek !== 0 && dayOfWeek !== 6) {
          daysToAdd--;
        }
      }
      
      var formattedDate = currentDate.toLocaleDateString("pt-BR");
      
      var message = "Olá, XXX. \n\n" +
                    "Peço desculpas pelo atraso na solicitação.\n\n" +
                    "Já estamos dando andamento em sua solicitação de cancelamento.\n\n" +
                    "Agora é só aguardar que até o dia " + formattedDate + " o produto será cancelado. O estorno ocorre em até 2 dias em sua conta Pix.Esse prazo é contado após a finalização do cancelamento.\n\n" +
                    name + "\n" +
                    "MediAção | Magalu\n\n" +
                    "Ah, e quando você entender que resolvemos a sua solicitação, peço que encerre o protocolo e avalie meu atendimento.\n" +
                    "Sua nota é muito importante para nós, tá?";
      
      // Copia a mensagem para a área de transferência
      navigator.clipboard.writeText(message)
        .then(function() {
          ;
        })
        .catch(function(error) {
          console.error("Erro ao copiar a mensagem: ", error);
        });
    }
  </script>
</body>
</html>
