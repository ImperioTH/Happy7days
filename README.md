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
            text-align: center;
        }
        header {
            width: 100%;
            padding: 20px;
            background-color: #1e1e1e;
        }
        header img {
            max-width: 150px;
            cursor: pointer;
        }
        header p {
            margin-top: 10px;
            color: #bdc3c7;
            font-size: 1.2rem;
        }
        nav {
            width: 100%;
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
            max-width: 1200px;
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
        #carrinho-container, #checkout-form {
            background-color: #1e1e1e;
            border-radius: 10px;
            padding: 20px;
            max-width: 350px;
        }
        #checkout-form input {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #34495e;
            border-radius: 5px;
        }
        .btn-submit {
            width: 100%;
            padding: 12px;
            background-color: #27ae60;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .btn-submit:hover {
            background-color: #2ecc71;
        }
    </style>
</head>
<body>
    <header>
        <img src="https://i.ibb.co/YPVm0fz/frSG2H8.jpg" alt="Logo Império TH" onclick="recarregarPagina()">
        <p>O IMPÉRIO DAS PRATAS!</p>
    </header>
    <nav>
        <a href="#">Home</a>
        <a href="#">Produtos</a>
        <a href="#">Contato</a>
    </nav>
    <div class="container">
        <h2>Promoções Especiais</h2>
        <div class="product">
            <img src="https://via.placeholder.com/200" alt="Corrente Prata 925">
            <h3>Corrente Prata 925</h3>
            <p>R$ 149,90</p>
            <button class="btn" onclick="adicionarAoCarrinho('Corrente Prata 925', 149.90)">Adicionar ao Carrinho</button>
        </div>
        <div class="product">
            <img src="https://via.placeholder.com/200" alt="Pulseira Prata 925">
            <h3>Pulseira Prata 925</h3>
            <p>R$ 79,90</p>
            <button class="btn" onclick="adicionarAoCarrinho('Pulseira Prata 925', 79.90)">Adicionar ao Carrinho</button>
        </div>
        <div id="carrinho-container" class="container">
            <h2>Seu Carrinho</h2>
            <ul id="carrinho-itens"></ul>
            <p id="total-carrinho">Total: R$ 0,00</p>
            <button class="btn" onclick="mostrarCheckout()">Finalizar Compra</button>
            <button class="btn" onclick="limparCarrinho()">Limpar Carrinho</button>
        </div>
        <div id="checkout-form" style="display: none;">
            <h2>Dados do Cliente</h2>
            <input type="text" id="nome" placeholder="Nome completo">
            <input type="email" id="email" placeholder="E-mail">
            <input type="text" id="telefone" placeholder="Telefone">
            <input type="text" id="rua" placeholder="Rua">
            <input type="text" id="numero" placeholder="Número">
            <input type="text" id="bairro" placeholder="Bairro">
            <input type="text" id="cep" placeholder="CEP">
            <button class="btn-submit" onclick="confirmarPedido()">Confirmar Pedido</button>
        </div>
    </div>
    <footer>
        <p>Império TH &copy; 2025 - Todos os direitos reservados.</p>
    </footer>
    <script>
        function recarregarPagina() {
            location.reload();
        }

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

            carrinho.forEach(produto => {
                carrinhoItens.innerHTML += `<li>${produto.nome} - R$ ${produto.preco.toFixed(2)}</li>`;
                total += produto.preco;
            });

            totalCarrinho.innerText = `Total: R$ ${total.toFixed(2)}`;
        }

        function mostrarCheckout() {
            document.getElementById('checkout-form').style.display = 'block';
        }

        function confirmarPedido() {
            const nome = document.getElementById('nome').value;
            const email = document.getElementById('email').value;
            const telefone = document.getElementById('telefone').value;
            const rua = document.getElementById('rua').value;
            const numero = document.getElementById('numero').value;
            const bairro = document.getElementById('bairro').value;
            const cep = document.getElementById('cep').value;

            if (nome && email && telefone && rua && numero && bairro && cep) {
                alert(`Obrigado, ${nome}! Seu pedido foi confirmado.`);
                document.getElementById('checkout-form').style.display = 'none';
                limparCarrinho();
            } else {
                alert('Por favor, preencha todos os campos!');
            }
        }

        function limparCarrinho() {
            carrinho = [];
            atualizarCarrinho();
        }
    </script>
</body>
</html>
