# iPhone 17 Pro Max — Landing Page (HTML + CSS)

Este projeto é uma **landing page estática** (sem JavaScript) sobre o iPhone 17 Pro Max. A navegação e os efeitos visuais são feitos apenas com **HTML (estrutura)** e **CSS (estilo, layout e animações por hover)**.

---

## Estrutura do site

### 1) `index.html`
Contém toda a estrutura da página, dividida em seções:

- **Header / Navegação fixa**
  - Barra de navegação no topo, com links usando âncoras (`href="#..."`) para saltar entre seções.
  - Botões/links levam para: `home`, `qualidades`, `beneficios`, `precos`.

- **Hero (seção inicial)**
  - Apresenta o produto com tag “Novo”, título, descrição e dois botões (CTAs).
  - Exibe a imagem do iPhone.

- **Seção “Cores”**
  - Mostra 3 cards (Titânio Branco, Azul e Laranja).
  - Cada card tem imagem, texto e elementos visuais como brilho (glow) e indicador circular.

- **Seção “Qualidades Excepcionais”**
  - Grid com 6 cards, cada um com um ícone (SVG inline), título e texto explicativo.

- **Specs Banner**
  - Faixa com 4 destaques (48MP, 6,9, A19 Pro, 33h), exibidos em linha com flexbox.

- **Seção “Benefícios”**
  - Grid com 6 cards numerados (01 a 06), explicando benefícios do produto.

- **Seção “Apple Intelligence”**
  - Layout em duas colunas (texto + imagem) no desktop.
  - No mobile, o CSS reorganiza para uma coluna.
  - Lista de recursos com “check” feito via pseudo-elemento (`::before`).

- **Seção “Preços”**
  - Grade com 3 cards de armazenamento/preço.
  - Um card recebe destaque via classe extra (`.destaque`).
  - Inclui bloco adicional de **Trade In** na mesma seção.

- **Footer**
  - Estrutura em colunas com listas de links.
  - Parte inferior com copyright e links legais.

---

### 2) `style.css`
Define todo o visual do site. Principais responsabilidades:

- **Tema e variáveis CSS**
  - `:root` centraliza cores como `--primary`, `--background`, `--foreground`, etc.

- **Layout e responsividade**
  - Usa **flexbox** (ex.: hero, specs, menus/cards) e **grid** (ex.: qualidades, benefícios, preços, footer).
  - Media queries em `992px`, `768px` e `480px` ajustam número de colunas, empilhamento e alinhamentos.

- **Efeitos visuais (hover/transition)**
  - Cards de cores: `transform`, sombra e glow aumentam ao passar o mouse.
  - Cards de qualidade/benefícios/preços: elevam/realçam com hover.

- **Header com efeito “vidro”**
  - Barra fixa com `backdrop-filter: blur(...)` e fundo semi-transparente.

---

## Como o usuário navega
- A navegação entre seções acontece por **âncoras HTML** (`href="#home"`, `href="#precos"`, etc.).
- O CSS define `scroll-behavior: smooth;` para o deslocamento ser suave.

---

## Observação didática
Por ser um projeto estático:
- não há lógica de usuário,
- não existe atualização dinâmica de conteúdo,
- as interações são apenas visuais (hover/transitions) e a navegação é feita por links de âncora.

