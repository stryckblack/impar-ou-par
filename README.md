segunda parte de codigo atividade 07


<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Menu</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body class="bg-light">

<div class="container Menu">
    
    <div class="btn-group mb-4" role="group" aria-label="Menu de controle">
        <button type="button" class="btn btn-primary" id="opcao1">🍕 Pizza</button>
        <button type="button" class="btn btn-success" id="opcao2">🏖️ Praia</button>
        <button type="button" class="btn btn-warning" id="opcao3">🚀 Espaço</button>
    </div>

    <div class="card" id="conteudo">
        <div class="card-body">
            <h5 class="card-title" id="titulo">Bem-vindo!</h5>
            <p class="card-text" id="texto">Clique em um dos botões acima para mudar o conteúdo.</p>
        </div>
    </div>
</div>




<script>


    const conteudos = {
        opcao1: {
            titulo: "Deliciosa Pizza",
            texto: "Nada como uma pizza quentinha para alegrar o dia!"
        },
        opcao2: {
            titulo: "Dia na Praia",
            texto: "Sol, mar e areia... o paraíso te espera!"
        },
        opcao3: {
            titulo: "Exploração Espacial",
            texto: "Rumo às estrelas em uma nova aventura cósmica!"
        }
    };



    document.querySelectorAll(".btn-group button").forEach(botao => {
        botao.addEventListener("click", () => {
            const conteudo = conteudos[botao.id];
            document.getElementById("titulo").textContent = conteudo.titulo;
            document.getElementById("texto").textContent = conteudo.texto;
        });
    });


</script>

</body>
</html>
