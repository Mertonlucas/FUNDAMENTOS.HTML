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
