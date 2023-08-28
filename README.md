<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EXERCÍCIOS HTML</title>
    <link rel="stylesheet" href="styles.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

header {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 1rem 0;
}

nav {
    background-color: #444;
    color: #fff;
    padding: 0.5rem;
}

nav ul {
    list-style: none;
    padding: 0;
}

nav a {
    color: #fff;
    text-decoration: none;
    display: block;
    padding: 0.5rem 1rem;
}

section {
    padding: 2rem;
    border-top: 1px solid #ddd;
    border-bottom: 1px solid #ddd;
}

footer {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 1rem 0;
}

    <header>
        <h1><i class="fas fa-code"></i> Exercícios HTML</h1>
    </header>
    <nav>
        <ul>
            <li><a href="ESTRUTURANDO-EXERCICIO/Exercicios/TESTE.HTML"><i class="fas fa-file-alt"></i> 00 - teste</a></li>
        </ul>
    </nav>
    <section id="conteudo"></section>
    <footer>
        <p><i class="fas fa-laptop-code"></i> EXERCÍCIO WEB</p>
    </footer>
    <script>
        document.querySelectorAll('a').forEach(link => {
            const conteudo = document.getElementById('conteudo');

            link.onclick = function(e) {
                e.preventDefault();
                fetch(link.href)
                .then(resp => resp.text())
                .then(html => conteudo.innerHTML = html);
            }
        });
    </script>
</body>
</html>
