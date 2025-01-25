
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Império TH - Loja de Pratas</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #000;
            color: #fff;
        }
        header {
            background-color: #222;
            padding: 20px;
            text-align: center;
        }
        header h1 {
            color: #c0c0c0;
        }
        nav {
            background-color: #333;
            text-align: center;
            padding: 10px;
        }
        nav a {
            color: #c0c0c0;
            margin: 0 15px;
            text-decoration: none;
            font-size: 1.2rem;
        }
        .container {
            padding: 20px;
            text-align: center;
        }
        .product {
            border: 1px solid #555;
            margin: 20px;
            padding: 15px;
            display: inline-block;
            width: 200px;
            border-radius: 10px;
            background-color: #111;
        }
        .product img {
            width: 100%;
            border-radius: 10px;
        }
        .btn {
            margin-top: 10px;
            padding: 10px;
            background-color: #555;
            color: #fff;
            border: none;
            cursor: pointer;
            border-radius: 5px;
        }
        .btn:hover {
            background-color: #777;
        }
    </style>
</head>
<body>
    <header>
        <h1>Bem-vindo ao Império TH</h1>
        <p>A prata que fala por você!</p>
    </header>
    <nav>
        <a href="#">Home</a>
        <a href="#">Produtos</a>
        <a href="#">Contato</a>
    </nav>
    <div class="container">
        <h2>Promoções Especiais</h2>
        <!-- Produtos -->
        <div class="product">
            <img src="https://via.placeholder.com/200" alt="Produto 1">
            <h3>Corrente Prata 925</h3>
            <p>R$ 149,90</p>
            <button class="btn" onclick="adicionarAoCarrinho('Corrente Prata 925', 149.90)">Adicionar ao Carrinho</button>
        </div>
        <div class="product">
            <img src="https://via.placeholder.com/200" alt="Produto 2">
            <h3>Anel Prata Masculino</h3>
            <p>R$ 89,90</p>
            <button class="btn" onclick="adicionarAoCarrinho('Anel Prata Masculino', 89.90)">Adicionar ao Carrinho</button>
        </div>
        <div class="product">
            <img src="https://via.placeholder.com/200" alt="Produto 3">
            <h3>Pulseira Prata 925</h3>
            <p>R$ 129,90</p>
            <button class="btn" onclick="adicionarAoCarrinho('Pulseira Prata 925', 129.90)">Adicionar ao Carrinho</button>
        </div>
    </div>

    <!-- Script para o Carrinho -->
    <script>
        // Array para armazenar os itens do carrinho
        let carrinho = [];

        // Função para adicionar itens ao carrinho
        function adicionarAoCarrinho(nome, preco) {
            // Cria um objeto do produto
            const produto = {
                nome: nome,
                preco: preco
            };
            
            // Adiciona ao carrinho
            carrinho.push(produto);
            alert(`${nome} foi adicionado ao carrinho!`);
            
            // Atualiza o carrinho no console (para testes)
            console.log(carrinho);
        }
    </script>
</body>
</html>
