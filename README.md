# PROJETO-FACUL

Página inicial com apresentação

Seção de projetos

Menu interativo

Um pouco de animação com JS

<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Portfólio de Lucas Barcarol</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <nav>
      <h1>Lucas Barcarol</h1>
      <ul id="menu">
        <li><a href="#sobre">Sobre</a></li>
        <li><a href="#projetos">Projetos</a></li>
        <li><a href="#contato">Contato</a></li>
      </ul>
      <button id="toggleMenu">☰</button>
    </nav>
  </header>

  <section id="sobre">
    <h2>Sobre Mim</h2>
    <p>Olá! Sou Lucas, estudante e entusiasta de tecnologia. Este é um pequeno portfólio para mostrar meus projetos e habilidades.</p>
  </section>

  <section id="projetos">
    <h2>Meus Projetos</h2>
    <div class="cards">
      <div class="card">
        <h3>Projeto 1</h3>
        <p>Uma página web interativa feita com HTML, CSS e JavaScript.</p>
      </div>
      <div class="card">
        <h3>Projeto 2</h3>
        <p>Outro projeto simples mostrando habilidades em front-end.</p>
      </div>
      <div class="card">
        <h3>Projeto 3</h3>
        <p>Pequena aplicação web com funcionalidades básicas em JS.</p>
      </div>
    </div>
  </section>

  <section id="contato">
    <h2>Contato</h2>
    <p>Email: lucas@example.com</p>
    <p>GitHub: <a href="https://github.com/seu-usuario" target="_blank">github.com/seu-usuario</a></p>
  </section>

  <footer>
    <p>&copy; 2025 Lucas Barcarol</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>


/* Reset básico */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, sans-serif;
}

body {
  line-height: 1.6;
  background: #f4f4f4;
  color: #333;
}

/* Header */
header {
  background: #4CAF50;
  color: #fff;
  padding: 1rem 0;
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 90%;
  margin: auto;
}

nav ul {
  display: flex;
  list-style: none;
}

nav ul li {
  margin-left: 1.5rem;
}

nav ul li a {
  color: #fff;
  text-decoration: none;
  font-weight: bold;
}

#toggleMenu {
  display: none;
  font-size: 1.5rem;
  background: none;
  border: none;
  color: #fff;
  cursor: pointer;
}

/* Sections */
section {
  padding: 2rem 10%;
}

section h2 {
  margin-bottom: 1rem;
  color: #4CAF50;
}

.cards {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
}

.card {
  background: #fff;
  padding: 1rem;
  flex: 1 1 200px;
  border-radius: 8px;
  box-shadow: 0px 2px 5px rgba(0,0,0,0.2);
}

/* Footer */
footer {
  text-align: center;
  padding: 1rem;
  background: #333;
  color: #fff;
}

/* Responsivo */
@media(max-width: 768px) {
  nav ul {
    display: none;
    flex-direction: column;
    margin-top: 1rem;
  }

  nav ul.show {
    display: flex;
  }

  #toggleMenu {
    display: block;
  }
}


const toggleMenu = document.getElementById('toggleMenu');
const menu = document.getElementById('menu');

toggleMenu.addEventListener('click', () => {
  menu.classList.toggle('show');
});

📚 O que Aprendi com este Projeto

Estruturação de páginas web

Como organizar o HTML de forma semântica com <header>, <section> e <footer>.

Criar seções claras e fáceis de navegar.

Estilização com CSS

Uso de Flexbox para organizar cards e menus.

Criação de layouts responsivos que se adaptam a diferentes tamanhos de tela.

Aplicação de cores, sombras e bordas para deixar o visual mais agradável.

Interatividade com JavaScript

Manipulação do DOM para abrir e fechar o menu em telas pequenas.

Uso de eventos como click para interações simples.

Boas práticas de organização

Separar HTML, CSS e JS em arquivos diferentes.

Nomear arquivos e classes de forma clara e consistente.

Publicação de projetos

Como preparar o projeto para ser colocado no GitHub.

Entender como criar um portfólio que pode ser compartilhado online.

Responsividade e UX básica

Tornar o site acessível e agradável em celular, tablet e desktop.

Pensar na experiência do usuário ao navegar pelo menu e seções.
