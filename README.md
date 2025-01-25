<!DOCTYPE html>
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
            box-sizing: border-box; /* Importante para calcular corretamente o layout */
        }
        *, *::before, *::after {
            box-sizing: inherit; /* Faz com que todos os elementos herdem o box-sizing */
        }
        header {
            background-color: #222;
            padding: 20px;
            text-align: center;
        }
        header h1 {
            color: #c0c0c0;
            font-size: 2rem;
            margin: 0;
        }
        header p {
            text-align: center;
            margin: 0;
            padding: 5px;
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
            width: 100%; /* Ajuste flexível para dispositivos móveis */
            max-width: 300px; /* Para evitar o crescimento excessivo nos PCs */
            border-radius: 10px;
            background-color: #111;
            box-sizing: border-box;
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
        #carrinho-container {
            margin-top: 30px;
            padding: 20px;
            background-color: #222;
            border-radius: 10px;
            text-align: left;
        }
        #carrinho-container ul {
            list-style: none;
            padding: 0;
        }
        #carrinho-container li {
            margin: 10px 0;
            padding: 10px;
            background-color: #111;
            border-radius: 5px;
        }
        .btn-finalizar, .btn-limpar {
            margin-top: 10px;
            padding: 10px;
            background-color: #c00;
            color: #fff;
            border: none;
            cursor: pointer;
            border-radius: 5px;
        }
        .btn-finalizar:hover, .btn-limpar:hover {
            background-color: #f33;
        }
        #total-carrinho {
            margin-top: 10px;
            font-size: 1.2rem;
        }

        /* Responsivo: Para telas menores (celulares) */
        @media (max-width: 768px) {
            header h1 {
                font-size: 1.5rem;
            }
            nav a {
                display: block;
                margin: 10px 0;
                font-size: 1rem;
            }
            .container {
                padding: 10px;
            }
            .product {
                width: 100%; /* Garante que os produtos ocupem toda a largura disponível */
                max-width: 100%; /* Não limita a largura em telas pequenas */
            }
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
            <
