<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Site</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Meu Site</h1>
        <nav>
            <ul>
                <li><a href="#home">Início</a></li>
                <li><a href="#about">Sobre</a></li>
                <li><a href="#contact">Contato</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <section id="home">
            <h2>Home</h2>
            <p>Bem-vindo ao meu site!</p>
            <img src="https://via.placeholder.com/800x400" alt="Imagem de exemplo">
        </section>
        <section id="about">
            <h2>Sobre</h2>
            <p>Informações sobre mim e o propósito deste site.</p>
        </section>
        <section id="contact">
            <h2>Contato</h2>
            <form id="contactForm" action="/submit" method="post">
                <label for="name">Nome:</label>
                <input type="text" id="name" name="name" required>
                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required>
                <label for="message">Mensagem:</label>
                <textarea id="message" name="message" required></textarea>
                <button type="submit">Enviar</button>
            </form>
        </section>
    </main>
    <footer>
        <p>&copy; 2024 Meu Site</p>
    </footer>
    <script src="script.js"></script>
</body>
</html>/* Reset básico */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    color: #333;
}

header {
    background: #333;
    color: #fff;
    padding: 10px 0;
    text-align: center;
}

header nav ul {
    list-style: none;
}

header nav ul li {
    display: inline;
    margin: 0 10px;
}

header nav ul li a {
    color: #fff;
    text-decoration: none;
}

main {
    padding: 20px;
}

section {
    margin-bottom: 20px;
}

section img {
    max-width: 100%;
    height: auto;
}

form {
    display: flex;
    flex-direction: column;
}

form label {
    margin: 10px 0 5px;
}

form input, form textarea {
    padding: 10px;
    margin-bottom: 10px;
}

form button {
    padding: 10px;
    background: #333;
    color: #fff;
    border: none;
    cursor: pointer;
}

footer {
    background: #333;
    color: #fff;
    text-align: center;
    padding: 10px 0;
    position: fixed;
    bottom: 0;
    width: 100%;
}

/* Animação de fade-in */
@keyframes fadeIn {
    from {
        opacity: 0;
    }
    to {
        opacity: 1;
    }
}

.fade-in {
    animation: fadeIn 2s ease-in;
}document.addEventListener('DOMContentLoaded', function() {
    console.log('Documento carregado e pronto para uso.');

    // Validação simples do formulário
    document.getElementById('contactForm').addEventListener('submit', function(event) {
        var email = document.getElementById('email').value;
        if (!email.includes('@')) {
            alert('Por favor, insira um email válido.');
            event.preventDefault(); // Impede o envio do formulário
        }
    });

    // Exemplo de uma função simples
    function greetUser() {
        alert('Bem-vindo ao Meu Site!');
    }

    // Chama a função
    greetUser();
});
