# PROJETO-FACUL

ndex.html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>To-Do List - Lucas Barcarol</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <h1>To-Do List</h1>

    <div class="input-container">
      <input type="text" id="novaTarefa" placeholder="Digite uma nova tarefa...">
      <button id="adicionarBtn">Adicionar</button>
    </div>

    <ul id="listaTarefas"></ul>
  </div>

  <script src="script.js"></script>
</body>
</html>

2️⃣ style.css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, sans-serif;
}

body {
  background-color: #f4f4f4;
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}

.container {
  background: #fff;
  padding: 2rem;
  border-radius: 10px;
  width: 90%;
  max-width: 400px;
  box-shadow: 0 4px 10px rgba(0,0,0,0.1);
}

h1 {
  text-align: center;
  color: #4CAF50;
  margin-bottom: 1.5rem;
}

.input-container {
  display: flex;
  margin-bottom: 1rem;
}

input[type="text"] {
  flex: 1;
  padding: 0.5rem;
  border: 2px solid #4CAF50;
  border-radius: 5px 0 0 5px;
  outline: none;
}

button {
  padding: 0.5rem 1rem;
  border: none;
  background-color: #4CAF50;
  color: #fff;
  font-weight: bold;
  cursor: pointer;
  border-radius: 0 5px 5px 0;
}

button:hover {
  background-color: #45a049;
}

ul {
  list-style: none;
}

li {
  background: #f9f9f9;
  margin-bottom: 0.5rem;
  padding: 0.5rem;
  border-radius: 5px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

li.completed {
  text-decoration: line-through;
  color: #888;
}

li button {
  background-color: #ff4d4d;
  border-radius: 5px;
  padding: 0.2rem 0.5rem;
}

li button:hover {
  background-color: #e60000;
}

3️⃣ script.js
const adicionarBtn = document.getElementById('adicionarBtn');
const novaTarefa = document.getElementById('novaTarefa');
const listaTarefas = document.getElementById('listaTarefas');

adicionarBtn.addEventListener('click', adicionarTarefa);
novaTarefa.addEventListener('keypress', function(e) {
  if(e.key === 'Enter') adicionarTarefa();
});

function adicionarTarefa() {
  const tarefaTexto = novaTarefa.value.trim();
  if(tarefaTexto === '') return;

  const li = document.createElement('li');
  li.textContent = tarefaTexto;

  li.addEventListener('click', () => {
    li.classList.toggle('completed');
  });

  const removerBtn = document.createElement('button');
  removerBtn.textContent = 'X';
  removerBtn.addEventListener('click', () => {
    li.remove();
  });

  li.appendChild(removerBtn);
  listaTarefas.appendChild(li);

  novaTarefa.value = '';
}

4️⃣ README.md
# 📝 To-Do List - Projeto de Portfólio

## Descrição
Uma aplicação web simples para gerenciar tarefas do dia a dia.  
O usuário pode **adicionar tarefas**, **marcar como concluídas** e **remover tarefas finalizadas**.  

Este projeto é ideal para quem quer **praticar HTML, CSS e JavaScript**, além de mostrar um exemplo funcional de aplicação para o portfólio.

---

## 🎯 Objetivo
O objetivo deste projeto é **praticar e demonstrar habilidades em desenvolvimento frontend**, aplicando conceitos de:  

- Estruturação de páginas com HTML semântico.  
- Estilização e responsividade com CSS.  
- Interatividade e lógica de programação com JavaScript.  

Além disso, serve como exemplo de **projeto completo** para incluir no portfólio e compartilhar no GitHub.

---

## 🛠 Tecnologias Utilizadas
- **HTML5** → Estrutura da página.  
- **CSS3** → Estilização, cores, layout e responsividade.  
- **JavaScript** → Manipulação do DOM, eventos e lógica do app.

---

## 📚 O que Aprendi
Durante o desenvolvimento deste projeto, aprendi a:  

1. **Criar uma página web funcional** com HTML e CSS.  
2. **Manipular elementos do DOM** para adicionar, marcar e remover tarefas dinamicamente.  
3. **Trabalhar com eventos em JavaScript**, como `click` e `keypress`.  
4. **Criar interatividade simples**, como marcar tarefas concluídas ou removê-las.  
5. **Organizar arquivos e código** de forma clara e modular.  
6. **Pensar em UX básica**, garantindo que o usuário consiga usar a aplicação de forma intuitiva.  
7. **Publicar projetos no GitHub**, tornando-os acessíveis online para portfólio.

---

## ▶️ Como Executar o Projeto
1. Clone o repositório:  
```bash
git clone https://github.com/seu-usuario/todo-list.git
