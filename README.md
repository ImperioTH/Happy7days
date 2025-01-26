<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Império TH - Loja de Pratas</title>
    <style>
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
            height: 100vh;
            text-align: center;
        }
        header {
            background-color: #1e1e1e;
            padding: 20px;
            width: 100%;
            max-width: 1200px;
        }
        header h1 {
            color: #f1c40f;
            font-size: 3rem;
            margin-bottom: 10px;
        }
        header p {
            color: #bdc3c7;
            font-size: 1.2rem;
        }
        nav {
            background-color: #34495e;
            padding: 15px;
            width: 100%;
            max-width: 1200px;
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
        .product {
            border: 1px solid #7f8c8d;
            margin: 20px auto;
            padding: 15px;
            border-radius: 10px;
            background-color: #2c3e50;
            max-width: 320px;
            transition: transform 0.3s;
        }
        .product:hover {
            transform: scale(1.05);
        }
        .product img {
            width: 100%;
            height: auto;
            border-radius: 10px;
            margin-bottom: 15px;
        }
        .product h3 {
            color: #f1c40f;
            font-size: 1.5rem;
            margin: 10px 0;
        }
        .product p {
            color: #ecf0f1;
            font-size: 1.2rem;
        }
        .btn {
            margin-top: 10px;
            padding: 12px;
            background-color: #f39c12;
            color: #fff;
            border: none;
            cursor: pointer;
            border-radius: 5px;
            transition: background-color 0.3s;
        }
        .btn:hover {
            background-color: #e67e22;
        }
        #carrinho-container {
            margin-top: 30px;
            padding: 20px;
            background-color: #1e1e1e;
            border-radius: 10px;
            max-width: 350px;
            margin: 30px auto;
        }
        #carrinho-container ul {
            list-style: none;
            padding: 0;
        }
        #carrinho-container li {
            margin: 15px 0;
            padding: 10px;
            background-color: #34495e;
            border-radius: 5px;
            color: #fff;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .btn-finalizar, .btn-limpar {
            margin-top: 15px;
            padding: 12px;
            background-color: #c0392b;
            color: #fff;
            border: none;
            cursor: pointer;
            border-radius: 5px;
            transition: background-color 0.3s;
        }
        .btn-finalizar:hover, .btn-limpar:hover {
            background-color: #e74c3c;
        }
        #total-carrinho {
            margin-top: 10px;
            font-size: 1.3rem;
            font-weight: bold;
            color: #f39c12;
        }
        footer {
            background-color: #1e1e1e;
            padding: 15px;
            margin-top: 20px;
            width: 100%;
            max-width: 1200px;
        }
        footer p {
            color: #bdc3c7;
            font-size: 1rem;
        }
    </style>
</head>
<body>
    <header>
        <h1>Bem-vindo ao Império TH</h1>
        <p>O IMPÉRIO DAS PRATAS!</p>
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

        <!-- Produtos de Fantasia -->
        <div class="product">
            <img src="https://via.placeholder.com/200" alt="Produto 4">
            <h3>Máscara Fantasia Prata</h3>
            <p>R$ 199,90</p>
            <button class="btn" onclick="adicionarAoCarrinho('Máscara Fantasia Prata', 199.90)">Adicionar ao Carrinho</button>
        </div>
        <div class="product">
            <img src="https://via.placeholder.com/200" alt="Produto 5">
            <h3>Coroa de Prata para Fantasia</h3>
            <p>R$ 299,90</p>
            <button class="btn" onclick="adicionarAoCarrinho('Coroa de Prata para Fantasia', 299.90)">Adicionar ao Carrinho</button>
        </div>
        <div class="product">
            <img src="https://via.placeholder.com/200" alt="Produto 6">
            <h3>Bracelete Fantasia de Prata</h3>
            <p>R$ 109,90</p>
            <button class="btn" onclick="adicionarAoCarrinho('Bracelete Fantasia de Prata', 109.90)">Adicionar ao Carrinho</button>
        </div>
        <!-- Carrinho -->
        <div id="carrinho-container" class="container">
            <h2>Seu Carrinho</h2>
            <ul id="carrinho-itens"></ul>
            <p id="total-carrinho">Total: R$ 0,00</p>
            <button class="btn-finalizar" onclick="finalizarCompra()">Finalizar Compra</button>
            <button class="btn-limpar" onclick="limparCarrinho()">Limpar Carrinho</button>
        </div>
    </div>

    <footer>
        <p>Império TH &copy; 2025 - Todos os direitos reservados.</p>
    </footer>

    <script>
        let carrinho = [];

        function adicionarAoCarrinho(nome, preco) {
            const produto = { nome, preco };
            carrinho.push(produto);
            atualizarCarrinho();
            alert(`${nome} foi adicionado ao carrinho!`);
        }

        function atualizarCarrinho() {
            const carrinhoItens = document.getElementById('carrinho-itens');
            const totalCarrinho = document.getElementById('total-carrinho');
            carrinhoItens.innerHTML = '';
            let total = 0;

            carrinho.forEach((produto, index) => {
                carrinhoItens.innerHTML += `<li>${produto.nome} - R$ ${produto.preco.toFixed(2)} 
                <button onclick="removerDoCarrinho(${index})" style="margin-left: 10px; color: red;">Remover</button></li>`;
                total += produto.preco;
            });

            totalCarrinho.innerText = `Total: R$ ${total.toFixed(2)}`;
        }

        function removerDoCarrinho(index) {
            carrinho.splice(index, 1);
            atualizarCarrinho();
        }

        function finalizarCompra() {
            if (carrinho.length > 0) {
                alert('Compra finalizada com sucesso!');
                carrinho = [];
                atualizarCarrinho();
            } else {
                alert('Seu carrinho está vazio!');
            }
        }

        function limparCarrinho() {
            carrinho = [];
            atualizarCarrinho();
        }
    </script>
</body>
</html>
