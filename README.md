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
            text-align: center;
        }
        header, nav, footer {
            width: 100%;
            max-width: 1200px;
        }
        header {
            background-color: #1e1e1e;
            padding: 20px;
        }
        header img {
            width: 300px;
            display: block;
            margin: 0 auto 10px;
        }
        header h1 {
            color: #f1c40f;
            font-size: 3rem;
        }
        header p {
            color: #bdc3c7;
            font-size: 1.2rem;
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
        
        /* Novos estilos para cards de categoria */
        .categorias-container {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
            margin: 30px 0;
        }
        
        .categoria-card {
            position: relative;
            border-radius: 10px;
            overflow: hidden;
            transition: transform 0.3s;
        }
        
        .categoria-card img {
            width: 100%;
            height: 100px;
            object-fit: cover;
            filter: brightness(0.7);
        }
        
        .categoria-card:hover {
            transform: translateY(-5px);
        }
        
        .categoria-btn {
            position: absolute;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            padding: 12px 30px;
            background-color: #f39c12;
            color: #fff;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            font-size: 1.2rem;
            text-decoration: none;
            transition: background-color 0.3s;
        }
        
        .categoria-btn:hover {
            background-color: #e67e22;
        }
        
        .product-categoria {
            margin: 40px 0;
            padding: 20px;
            background-color: #1a1a1a;
            border-radius: 10px;
        }
        
        .products-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
            margin-top: 20px;
        }
        
        .product {
            background-color: #2c3e50;
            border-radius: 10px;
            padding: 15px;
            transition: transform 0.3s;
        }
        
        .product:hover {
            transform: translateY(-5px);
        }
        
        .product img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            border-radius: 8px;
        }
        
        /* Estilos do carrinho mantidos */
        #carrinho-container {
            background-color: #1e1e1e;
            border-radius: 10px;
            padding: 20px;
            max-width: 350px;
            margin: 40px auto;
        }
        
        #checkout-form {
            display: none;
            background-color: #1e1e1e;
            border-radius: 10px;
            padding: 20px;
            max-width: 350px;
            margin: 20px auto;
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
        
        .btn {
            margin-top: 10px;
            padding: 12px;
            background-color: #f39c12;
            color: #fff;
            border: none;
            cursor: pointer;
            border-radius: 5px;
            width: 100%;
        }
        
        html {
            scroll-behavior: smooth;
        }
        
        @media (max-width: 768px) {
            .categorias-container {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <img src="https://i.postimg.cc/3N0Njn3m/20250114-025227-0000.png" alt="Logo Império TH">
        <h1>SEJA BEM-VINDO</h1>
        <p>AO NOSSO IMPÉRIO!</p>
    </header>
    <nav>
        <a href="#">Home</a>
        <a href="#">Produtos</a>
        <a href="#">Contato</a>
    </nav>
    <div class="container">
        <h2>Pratas</h2>
        
        <!-- Cards de Categorias -->
        <div class="categorias-container">
            <a href="#correntes" class="categoria-card">
                <img src="https://via.placeholder.com/400x250/2c3e50/fff?text=Correntes+em+Prata" alt="Correntes">
                <button class="categoria-btn">Correntes</button>
            </a>
            
            <a href="#aneis" class="categoria-card">
                <img src="">
                <button class="categoria-btn">Anéis</button>
            </a>
            
            <a href="#brincos" class="categoria-card">
                <img src="https://via.placeholder.com/400x250/2c3e50/fff?text=Brincos+Modernos" alt="Brincos">
                <button class="categoria-btn">Brincos</button>
            </a>
        </div>

        <!-- Seção Correntes -->
        <div class="product-categoria" id="correntes">
            <h3>Correntes em Prata 925</h3>
            <div class="products-container">
                <div class="product">
                    <img src="https://via.placeholder.com/300x200/34495e/fff?text=Corrente+Fina" alt="Corrente Fina">
                    <h4>Corrente Prata Fina</h4>
                    <p>R$ 129,90</p>
                    <button class="btn" onclick="adicionarAoCarrinho('Corrente Fina', 129.90)">Comprar</button>
                </div>
                <div class="product">
                    <img src="https://via.placeholder.com/300x200/34495e/fff?text=Corrente+Grossa" alt="Corrente Grossa">
                    <h4>Corrente Prata Grossa</h4>
                    <p>R$ 179,90</p>
                    <button class="btn" onclick="adicionarAoCarrinho('Corrente Grossa', 179.90)">Comprar</button>
                </div>
            </div>
        </div>

        <!-- Seção Anéis -->
        <div class="product-categoria" id="aneis">
            <h3>Anéis em Prata 925</h3>
            <div class="products-container">
                <div class="product">
                    <img src="https://via.placeholder.com/300x200/34495e/fff?text=Anel+Simples" alt="Anel Simples">
                    <h4>Anel Prata Simples</h4>
                    <p>R$ 89,90</p>
                    <button class="btn" onclick="adicionarAoCarrinho('Anel Simples', 89.90)">Comprar</button>
                </div>
                <div class="product">
                    <img src="https://via.placeholder.com/300x200/34495e/fff?text=Anel+Pedra" alt="Anel com Pedra">
                    <h4>Anel com Pedra</h4>
                    <p>R$ 149,90</p>
                    <button class="btn" onclick="adicionarAoCarrinho('Anel com Pedra', 149.90)">Comprar</button>
                </div>
            </div>
        </div>

        <!-- Seção Brincos -->
        <div class="product-categoria" id="brincos">
            <h3>Brincos em Prata 925</h3>
            <div class="products-container">
                <div class="product">
                    <img src="https://via.placeholder.com/300x200/34495e/fff?text=Brinco+Bolinha" alt="Brinco Bolinha">
                    <h4>Brinco Bolinha Prata</h4>
                    <p>R$ 69,90</p>
                    <button class="btn" onclick="adicionarAoCarrinho('Brinco Bolinha', 69.90)">Comprar</button>
                </div>
                <div class="product">
                    <img src="https://via.placeholder.com/300x200/34495e/fff?text=Brinco+Argola" alt="Brinco Argola">
                    <h4>Brinco Argola Grande</h4>
                    <p>R$ 99,90</p>
                    <button class="btn" onclick="adicionarAoCarrinho('Brinco Argola', 99.90)">Comprar</button>
                </div>
            </div>
        </div>

        <!-- Carrinho de Compras (MANTIDO DO CÓDIGO ORIGINAL) -->
        <div id="carrinho-container">
            <h2>Seu Carrinho</h2>
            <ul id="carrinho-itens"></ul>
            <p id="total-carrinho">Total: R$ 0,00</p>
            <button class="btn" onclick="mostrarCheckout()">Finalizar Compra</button>
            <button class="btn" onclick="limparCarrinho()">Limpar Carrinho</button>
        </div>

        <!-- Formulário de Checkout (MANTIDO DO CÓDIGO ORIGINAL) -->
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
        // JavaScript COMPLETO do código original + melhorias
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
            alert("Carrinho limpo com sucesso!");
        }
    </script>
</body>
</html>
