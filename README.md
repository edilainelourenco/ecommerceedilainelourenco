# ecommerceedilainelourenco
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Isa Fru Fru</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
<header>
        <button id="btn-menu">Menu</button>
        <nav id="menu" class="menu">
            <a href="#vitrine">Produtos</a>
            <a href="#contato">Contato</a>
        </nav>
    </header>

  <section class="banner">
        <h2>Isa Fru Fru</h2>
        <p id="aviso-frete"></p>
    </section>

  <section id="vitrine" class="container">
        <div class="produtos">
            <div class="cartao">
                <img src="imagem1.png" alt="Tiara Cereja">
                <p>Produto 1</p>
                <p>R$ 59,90</p>
            </div>
            <div class="cartao">
                <img src="IMG_20260927_172430_685.jpg" alt="Parzinho Cereja">
                <p>Produto 2</p>
                <p>R$ 39,90</p>
            </div>
            <div class="cartao">
                <img src="IMG_20260927_172432_331.jpg" alt="Tiara Bebê">
                <p>Produto 3</p>
                <p>R$ 49,90</p>
            </div>
        </div>
    </section>

   <section id="contato" class="container">
        <form id="contato-form">
            <input id="email" type="text" placeholder="Seu e-mail">
            <button type="submit">Enviar</button>
            <p id="erro"></p>
        </form>
    </section>

  <footer>
        <p>contato@isafrufru.com</p>
    </footer>

  <script src="js/app.js" defer></script>
</body>
</html>


const totalCarrinho = 250;
const aviso = document.querySelector("#aviso-frete");

if (totalCarrinho >= 200) {
    aviso.textContent = "Frete grátis!";
} else {
    aviso.textContent = "Frete: R$ 20";
}


const btn = document.querySelector("#btn-menu");
const menu = document.querySelector("#menu");

btn.addEventListener("click", function () {
    menu.classList.toggle("aberto");
});

const form = document.querySelector("#contato-form");
const email = document.querySelector("#email");
const erro = document.querySelector("#erro");

form.addEventListener("submit", function (evento) {
    if (email.value === "") {
        evento.preventDefault();
        erro.textContent = "Digite seu e-mail.";
    }
});
