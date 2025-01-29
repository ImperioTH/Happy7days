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
        .logo {
            width: 200px; /* Ajuste conforme necessário */
            height: auto;
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
    </style>
</head>
<body>
    <header>
        <img src="https://i.postimg.cc/3N0Njn3m/20250114-025227-0000.png" alt="Logo Império TH" class="logo">
        <p>O IMPÉRIO DAS PRATAS!</p>
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
        <div id="carrinho-container">
            <h2>Seu Carrinho</h2>
            <ul id="carrinho-itens"></ul>
            <p id="total-carrinho">Total: R$ 0,00</p>
            <button class="btn" onclick="mostrarCheckout()">Finalizar Compra</button>
            <button class="btn" onclick="limparCarrinho()">Limpar Carrinho</button>
        </div>
        <div id="checkout-form">
            <h2>Dados do Cliente</h2>
            <h3>Dados Pessoais</h3>
            <input type="text" id="nome" placeholder="Nome completo">
            <input type="email" id="email" placeholder="E-mail">
            <input type="text" id="telefone" placeholder="Telefone">
            <h3>Endereço</h3>
            <input type="text" id="rua" placeholder="Rua">
            <input type="text" id="numero" placeholder="Número">
            <input type="text" id="bairro" placeholder="Bairro">
            <input type="text" id="complemento" placeholder="Complemento (opcional)">
            <input type="text" id="cep" placeholder="CEP">
            <button class="btn-submit" onclick="confirmarPedido()">Confirmar Pedido</button>
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

            carrinho.forEach((produto) => {
                carrinhoItens.innerHTML += `<li>${produto.nome} - R$ ${produto.preco.toFixed(2)}</li>`;
                total += produto.preco;
            });

            totalCarrinho.innerText = `Total: R$ ${total.toFixed(2)}`;
        }

        function mostrarCheckout() {
            const checkoutForm = document.getElementById('checkout-form');
            checkoutForm.style.display = 'block';
            window.scrollTo({ top: checkoutForm.offsetTop, behavior: 'smooth' });
        }

        function confirmarPedido() {
            const nome = document.getElementById('nome').value;
            const email = document.getElementById('email').value;
            const telefone = document.getElementById('telefone').value;
            const rua = document.getElementById('rua').value;
            const numero = document.getElementById('numero').value;
            const bairro = document.getElementById('bairro').value;
            const complemento = document.getElementById('complemento').value;
            const cep = document.getElementById('cep').value;

            if (nome && email && telefone && rua && numero && bairro && cep) {
                alert(`Obrigado, ${nome}! Seu pedido foi confirmado.`);
                document.getElementById('checkout-form').style.display = 'none';
                limparCarrinho();
            } else {
                alert('Por favor, preencha todos os campos obrigatórios!');
            }
        }

        function limparCarrinho() {
            carrinho = [];
            atualizarCarrinho();
        }
    </script>
</body>
</html>
