<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Império TH - Loja de Pratas</title>
    <style>
        /* Estilos do site */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Arial', sans-serif;
            background-color: #0a0a0a;
            color: #fff;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: flex-start;
            text-align: center;
        }
        header {
            background-color: #1e1e1e;
            padding: 20px;
        }
        header img {
            width: auto;
            height: 200px; /* Aumentei o tamanho da logo */
        }
        nav {
            background-color: #34495e;
            padding: 15px;
        }
        nav a {
            color: #ecf0f1;
            margin: 0 20px;
            text-decoration: none;
            font-size: 1.1rem;
            transition: color 0.3s;
        }
        nav a:hover {
            color: #f39c12;
        }
        .container {
            padding: 20px;
            width: 100%;
            max-width: 1200px;
        }
        .products-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
        }
        .product {
            border: 1px solid #7f8c8d;
            margin: 20px auto;
            padding: 15px;
            border-radius: 10px;
            background-color: #2c3e50;
            max-width: 320px;
        }
        .product img {
            width: 100%;
            border-radius: 10px;
        }
        .btn {
            margin-top: 10px;
            padding: 12px;
            background-color: #f39c12;
            color: #fff;
            border: none;
            cursor: pointer;
            border-radius: 5px;
        }
        .btn:hover {
            background-color: #e67e22;
        }
    </style>
</head>
<body>
    <header>
        <img src="https://i.postimg.cc/3N0Njn3m/20250114-025227-0000.png" alt="Logo Império TH">
    </header>
    <nav>
        <a href="#">Home</a>
        <a href="#">Produtos</a>
        <a href="#">Contato</a>
    </nav>
    <div class="container">
        <h2>Promoções Especiais</h2>
        <div class="products-container">
            <div class="product">
                <img src="https://via.placeholder.com/200" alt="Produto 1">
                <h3>Corrente Prata 925</h3>
                <p>R$ 149,90</p>
                <button class="btn" onclick="adicionarAoCarrinho('Corrente Prata 925', 149.90)">Adicionar ao Carrinho</button>
            </div>
            <div class="product">
                <img src="https://via.placeholder.com/200" alt="Produto 2">
                <h3>Pulseira Masculina</h3>
                <p>R$ 89,90</p>
                <button class="btn" onclick="adicionarAoCarrinho('Pulseira Masculina', 89.90)">Adicionar ao Carrinho</button>
            </div>
            <div class="product">
                <img src="https://via.placeholder.com/200" alt="Produto 3">
                <h3>Brinco de Prata</h3>
                <p>R$ 59,90</p>
                <button class="btn" onclick="adicionarAoCarrinho('Brinco de Prata', 59.90)">Adicionar ao Carrinho</button>
            </div>
        </div>
    </div>
    <footer>
        <p>Império TH &copy; 2025 - Todos os direitos reservados.</p>
    </footer>
</body>
</html>
