<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Império TH  Loja de Pratas</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <style>
        /* Adicionar customizações adicionais de estilo aqui, se necessário */
        body {
            font-family: Arial, sans-serif;
            background-color: #000;
            color: #fff;
        }
        /* Adicionando um toque mais limpo e profissional */
        .header-bg {
            background-color: #111;
        }
        .footer-bg {
            background-color: #222;
        }
        .product {
            border-radius: 10px;
            background-color: #111;
        }
        .btn {
            background-color: #333;
            color: white;
            border-radius: 8px;
            padding: 10px;
            transition: 0.3s;
        }
        .btn:hover {
            background-color: #555;
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header class="header-bg text-center py-6">
        <h1 class="text-4xl text-gray-200">Bem-vindo ao Império TH</h1>
        <p class="text-xl text-gray-400">O IMPÉRIO DAS PRATAS!</p>
    </header>

    <!-- Navbar -->
    <nav class="bg-gray-900 text-white py-4">
        <div class="container mx-auto flex justify-center">
            <a href="#" class="px-6">Home</a>
            <a href="#" class="px-6">Produtos</a>
            <a href="#" class="px-6">Contato</a>
        </div>
    </nav>

    <!-- Container de Produtos -->
    <div class="container mx-auto px-4 py-8">
        <h2 class="text-3xl text-center mb-8">Promoções Especiais</h2>
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
            <div class="product p-6 rounded-lg shadow-lg bg-gray-800">
                <img src="https://via.placeholder.com/200" alt="Produto 1" class="rounded-lg w-full mb-4">
                <h3 class="text-2xl text-white">Corrente Prata 925</h3>
                <p class="text-xl text-gray-400">R$ 149,90</p>
                <button class="btn w-full mt-4" onclick="adicionarAoCarrinho('Corrente Prata 925', 149.90)">Adicionar ao Carrinho</button>
            </div>
            <!-- Outros Produtos -->
        </div>
    </div>

    <!-- Carrinho -->
    <div id="carrinho-container" class="container mx-auto px-4 py-8">
        <h2 class="text-2xl text-center mb-4">Seu Carrinho</h2>
        <ul id="carrinho-itens" class="list-none mb-4">
            <!-- Itens do carrinho serão adicionados aqui -->
        </ul>
        <p id="total-carrinho" class="text-xl">Total: R$ 0,00</p>
        <button class="btn w-full mt-4" onclick="finalizarCompra()">Finalizar Compra</button>
    </div>

    <!-- Footer -->
    <footer class="footer-bg text-center py-4 mt-8">
        <p class="text-gray-400">Império TH &copy; 2025 - Todos os direitos reservados.</p>
    </footer>

    <!-- Script -->
    <script>
        let carrinho = [];

        function adicionarAoCarrinho(nome, preco) {
            const produto = { nome, preco };
            carrinho.push(produto);
            atualizarCarrinho();
        }

        function atualizarCarrinho() {
            const carrinhoItens = document.getElementById('carrinho-itens');
            const totalCarrinho = document.getElementById('total-carrinho');
            carrinhoItens.innerHTML = '';
            let total = 0;

            carrinho.forEach((produto, index) => {
                carrinhoItens.innerHTML += `<li class="bg-gray-700 p-4 mb-2 text-white flex justify-between items-center">${produto.nome} - R$ ${produto.preco.toFixed(2)} 
                <button onclick="removerDoCarrinho(${index})" class="text-red-500 ml-4">Remover</button></li>`;
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
    </script>

</body>
</html>
