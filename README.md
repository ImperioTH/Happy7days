<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Império TH</title>
    <link rel="icon" href="https://i.ibb.co/yFQ6F0n/logo-imperio.png" type="image/png">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: Arial, sans-serif;
            background-color: #0a0a0a;
            color: #fff;
        }
        header {
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: #1e1e1e;
            padding: 15px 0;
        }
        header img {
            max-height: 100px;
        }
        nav {
            background-color: #34495e;
            display: flex;
            justify-content: center;
            padding: 10px 0;
        }
        nav a {
            color: #ecf0f1;
            margin: 0 15px;
            text-decoration: none;
            font-size: 18px;
            transition: color 0.3s;
        }
        nav a:hover {
            color: #f39c12;
        }
        .container {
            padding: 20px;
            text-align: center;
        }
        .container h1 {
            margin-bottom: 20px;
        }
        .products {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }
        .product {
            border: 1px solid #7f8c8d;
            padding: 15px;
            border-radius: 10px;
            background-color: #2c3e50;
            width: 200px;
        }
        .product img {
            width: 100%;
            height: auto;
            border-radius: 10px;
        }
        .btn {
            margin-top: 10px;
            padding: 10px;
            background-color: #f39c12;
            color: #fff;
            border: none;
            cursor: pointer;
            border-radius: 5px;
        }
        .btn:hover {
            background-color: #e67e22;
        }
        footer {
            background-color: #1e1e1e;
            color: #7f8c8d;
            text-align: center;
            padding: 10px;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <header>
        <img src="https://i.ibb.co/yFQ6F0n/logo-imperio.png" alt="Logo Império TH">
    </header>
    <nav>
        <a href="#">Home</a>
        <a href="#">Produtos</a>
        <a href="#">Contato</a>
    </nav>
    <div class="container">
        <h1>Promoções Especiais</h1>
        <div class="products">
            <div class="product">
                <img src="https://via.placeholder.com/200" alt="Corrente Prata 925">
                <h3>Corrente Prata 925</h3>
                <p>R$ 149,90</p>
                <button class="btn">Adicionar ao Carrinho</button>
            </div>
            <div class="product">
                <img src="https://via.placeholder.com/200" alt="Pulseira Prata 925">
                <h3>Pulseira Prata 925</h3>
                <p>R$ 79,90</p>
                <button class="btn">Adicionar ao Carrinho</button>
            </div>
        </div>
    </div>
    <footer>
        <p>Império TH &copy; 2025 - Todos os direitos reservados.</p>
    </footer>
</body>
</html>
