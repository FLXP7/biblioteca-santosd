Projeto Biblioteca Virtual "Santos Dumont"
Descrição
Este é um projeto de uma página web simples e interativa para exibir o catálogo de livros da "Biblioteca Santos Dumont". A página principal apresenta uma galeria com os livros disponíveis e, ao clicar em um livro, o usuário é redirecionado para uma página de detalhes, que exibe informações completas como sinopse, autor, ano de publicação e número de páginas. Um recurso de destaque é a sinopse em áudio, que pode ser reproduzida ao clicar na capa do livro na página de detalhes.

O projeto foi desenvolvido com HTML, CSS e JavaScript puros, focando na manipulação do DOM para criar conteúdo dinamicamente a partir de um objeto JavaScript.

Funcionalidades
Catálogo Dinâmico: Os livros são carregados dinamicamente a partir de um objeto JavaScript, facilitando a adição ou remoção de novas obras.

Página de Detalhes: Cada livro possui uma página de detalhes dedicada, com informações completas.

Reprodutor de Áudio Interativo: Na página de detalhes, o usuário pode ouvir a sinopse do livro clicando na imagem da capa. Um ícone de play/pause aparece para controlar a reprodução.

Design Responsivo: A interface se adapta a diferentes tamanhos de tela, como desktops e dispositivos móveis.

Navegação Simples: A navegação é intuitiva, permitindo que o usuário explore o catálogo e volte facilmente.

Tecnologias Utilizadas
HTML5: Para a estrutura semântica das páginas.

CSS3: Para estilização, layout (Grid e Flexbox) e responsividade.

JavaScript: Para manipulação do DOM, criação dinâmica de conteúdo e interatividade do reprodutor de áudio.

Estrutura de Arquivos
Para que o projeto funcione corretamente, os arquivos devem estar organizados da seguinte forma:

/projeto-biblioteca
│
├── index.html            # Página principal que exibe o catálogo
├── detalhes.html         # Página que exibe os detalhes de um livro
├── style.css             # Folha de estilos principal
├── biblioteca.js         # Contém o objeto com os dados dos livros e a função do catálogo
├── detalhes.js           # Lógica da página de detalhes e do reprodutor de áudio
│
├── /images/              # Pasta para as imagens das capas dos livros
│   ├── onome_do_vento.jpg
│   ├── 1984.jpg
│   └── ...
│
└── /audio/               # Pasta para os arquivos de áudio das sinopses
    ├── onome_do_vento.mp3
    ├── 1984.mp3
    └── ...
Como Executar o Projeto
Como este é um projeto front-end estático, você não precisa de um servidor complexo para executá-lo.

Clone ou baixe este repositório para a sua máquina local.

Verifique a estrutura de arquivos para garantir que as pastas images e audio estão no lugar correto.

Abra o arquivo index.html no seu navegador de preferência (Google Chrome, Firefox, etc.).

Pronto! Navegue pelo catálogo e explore os detalhes dos livros.

Explicação do Código
biblioteca.js
Define o objeto biblioteca, que armazena todas as informações dos livros (título, autor, capa, sinopse, áudio, etc.).

Contém a função exibirCatalogo(), que percorre a lista de livros e cria dinamicamente os "cards" de cada livro na página index.html.

A função é executada automaticamente quando a página principal é carregada (window.onload).

detalhes.js
Este script é executado na página detalhes.html.

Ele captura o id do livro a partir do parâmetro na URL (ex: detalhes.html?id=0).

Usa esse id para encontrar o livro correspondente no objeto biblioteca (que é importado através do biblioteca.js).

Preenche dinamicamente a página com as informações do livro selecionado.

Adiciona os eventos de clique e mouseover à capa do livro para controlar a reprodução do áudio da sinopse.

style.css
Responsável por toda a aparência visual do projeto.

Utiliza Grid Layout (display: grid) para organizar o catálogo de livros na página principal.

Utiliza Flexbox (display: flex) para alinhar os elementos na página de detalhes.

Inclui uma media query (@media (max-width: 768px)) para garantir que o layout se ajuste bem em telas menores.

Autor
Felipe Oliveira Silva