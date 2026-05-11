# Documentação do Projeto: Biolab

## Visão Geral

O **Biolab** é uma landing page institucional desenvolvida para apresentar uma empresa do setor farmacêutico, destacando sua inovação, credibilidade e compromisso com a qualidade de vida. O projeto possui um design moderno e responsivo, com seções bem definidas que incluem um cabeçalho interativo, conteúdo multimídia, efeito parallax, estatísticas, avaliações de profissionais, formulário de contato e rodapé informativo.

O projeto foi construído com **HTML5** e **CSS3**, utilizando boas práticas de organização, variáveis CSS, fontes do Google Fonts e transições suaves.

## Tecnologias Utilizadas

- **HTML5**: Estruturação semântica do conteúdo.
- **CSS3**: Estilização completa, incluindo layout flexível, efeito parallax e design responsivo.
- **Google Fonts**: Fontes externas (*Inter* e *Roboto*) para melhor tipografia.
- **Imagens e vídeos locais**: Recursos visuais armazenados em pastas organizadas (`assets/images` e `assets/videos`).

## Estrutura de Arquivos

```
project-root/
│
├── index.html
├── src/
│   ├── styles/
│   │   ├── global.css
│   │   └── style.css
│   ├── assets/
│   │   ├── images/
│   │   └── videos/
└── README.md (esta documentação)
```

## Arquivos CSS

### 1. `global.css` – Reset e Variáveis Globais

#### Função
Arquivo responsável por resetar os estilos padrão dos navegadores e definir variáveis CSS globais (cores, fontes, tamanhos e pesos).

#### Principais Definições

- **Reset**: Remove margens, paddings, bordas e define `box-sizing: border-box` para todos os elementos.
- **Variáveis de cores**:
  - `--color-white`, `--color-black`, `--color-blue`, `--color-dark-blue`, `--color-green`, `--color-dark-green`, `--color-yellow`.
- **Fontes**:
  - `--font-body`: "Inter"
  - `--font-title`: "Roboto"
- **Tamanhos de fonte**:
  - `--font-size-p`: 16px
  - `--font-size-h1`: 54px
  - `--font-size-h2`: 44px
  - `--font-size-h3`: 36px
  - `--font-size-h4`: 30px
- **Pesos de fonte**:
  - `--font-w-p`: 400
  - `--font-w-a`: 600
  - `--font-w-h`: 700

### 2. `style.css` – Estilização da Página

#### Função
Define todos os estilos visuais da página, incluindo layout, cores, espaçamentos, efeitos e responsividade.

#### Seções estilizadas

##### Cabeçalho (`<header>`)
- Layout flexível com espaçamento entre logo, navegação e botão de contato.
- Botão com hover suave e transição de cor.
- Links de navegação sem sublinhado e com fonte definida.

##### Conteúdo Principal (`<main>`)
- Seção `.home`: vídeo institucional e formulário de inscrição por e-mail.
- Formulário com campo de e-mail e botão estilizado com efeito hover.

##### Efeito Parallax (`.content-parallax`)
- Imagem de fundo fixa com sobreposição escura (`linear-gradient`).
- Altura personalizada e comportamento `background-attachment: fixed`.

##### Estatísticas (`.content-statistics`)
- Título com destaque em azul.
- Três cards com imagens, números e descrições, com diferentes `margin-top` para efeito escada.

##### Avaliações Profissionais (`.reviews`)
- Cards com avaliações de profissionais da saúde.
- Cada card contém estrelas (imagens), depoimento, foto e nome do profissional.
- Layout flexível com borda e espaçamento interno.

##### Contato (`.contact`)
- Três cards com ícones (e-mail, telefone, localização).
- Títulos e textos descritivos.
- Endereço e e-mail com destaque.

##### Rodapé (`<footer>`)
- Logo, links de navegação repetidos, divisor visual.
- Seção de direitos autorais e links para políticas e termos.
- Layout flexível com alinhamento entre colunas.

## Estrutura do `index.html`

### Cabeçalho
- Navegação com links âncora para as seções da página.
- Logo da empresa.
- Botão "Fale Conosco" com link para seção de contato.

### Conteúdo Principal
1. **Home** (`<section class="home">`):
   - Vídeo com controles e poster.
   - Título, descrição e formulário de inscrição.

2. **Parallax** (`<div class="content-parallax">`):
   - Seções vazias apenas para efeito visual com imagem fixa.

3. **Estatísticas** (`<section class="content-statistics">`):
   - Texto institucional.
   - Três imagens com informações de tempo de mercado, produtos e funcionários.

4. **Avaliações** (`<section class="reviews">`):
   - Três cards de depoimentos com estrelas, fotos e cargos.

5. **Contato** (`<section class="contact">`):
   - Cards com e-mail, telefone e endereço.

### Rodapé
- Logo, navegação secundária, divisor, direitos reservados e links legais.

## Como Executar o Projeto

1. Faça o download ou clone o repositório.
2. Certifique-se de que a estrutura de pastas esteja mantida, principalmente os diretórios `src/styles` e `src/assets`.
3. Abra o arquivo `index.html` em qualquer navegador moderno.

> **Nota:** O projeto não depende de servidor backend ou banco de dados. O formulário de e-mail não envia dados – é apenas estático.

## Personalização

### Alterando Cores
Edite as variáveis na seção `:root` do arquivo `global.css`.

### Substituindo Imagens e Vídeos
- **Logo**: substitua `logo-biolab.svg` na pasta `assets/images`.
- **Vídeo**: substitua `video-biolab.mp4` e a imagem de poster (`capa-video-biolab.png`).
- **Imagens das estatísticas**: substitua os arquivos `estatisticas-img-1.svg`, `estatisticas-img-2.svg`, `estatisticas-img-3.svg`.
- **Avaliações**: substitua as fotos `avaliacao-img-1.svg`, `avaliacao-img-2.svg`, `avaliacao-img-3.svg`.
- **Ícones de contato**: substitua os arquivos `logo-email.svg`, `logo-telefone.svg`, `logo-local.svg`.
- **Estrelas**: mantenha `review-star.png` ou substitua por outro ícone.

### Ajustando Efeito Parallax
- Altere a imagem no CSS: `.content-parallax > section:nth-of-type(2)`.
- Modifique a altura, opacidade do gradiente ou remova/adicione seções conforme necessário.