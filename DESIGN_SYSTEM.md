# 🎨 Design System - Refatoração Front-End Labs

Este projeto foi completamente refatorado para seguir um padrão de **Design System moderno, fluído e baseado em componentes reutilizáveis**, mantendo as características originais do projeto.

## 📋 Estrutura do Projeto

```
css/
├── reset.css          # Reset CSS normalizado
├── tokens.css         # Variáveis globais e tokens de design
├── base.css           # Estilos base para elementos HTML5
├── layout.css         # Sistema de grid, containers e espaçamento
├── components.css     # Componentes reutilizáveis (BEM Pattern)
├── utils.css          # Classes utilitárias
├── about.css          # Estilos específicos da página about
└── style.css          # Arquivo importador centralizado

html/
├── index.html         # Página inicial (Home)
├── about.html         # Página sobre (Sobre Nós)
├── classes.html       # Página de aulas/cursos
└── README.md          # Esta documentação
```

---

## 🎯 Características do Design System

### 1. **Tokens de Design** (`tokens.css`)
- **Cores**: Paleta completa (primária, secundária, status)
- **Tipografia**: Família, pesos, tamanhos e alturas de linha
- **Espaçamento**: Sistema de escala consistente (xs, sm, md, lg, xl, 2xl, 3xl)
- **Bordas**: Raios, larguras e estilos
- **Sombras**: Variações para profundidade
- **Z-index**: Camadas organizadas
- **Transições**: Velocidades padronizadas

### 2. **Padrão BEM (Block Element Modifier)**
Nomenclatura consistente para classes:
```html
<!-- BLOCO -->
<div class="footer">
  <!-- ELEMENTO -->
  <img class="footer__logo" />
  <!-- MODIFICADOR -->
  <p class="footer__text">Texto</p>
</div>
```

### 3. **Componentes Reutilizáveis**

#### Header
```html
<header class="header">
  <div class="container">
    <div class="header__container">
      <img class="header__logo" />
      <nav class="header__nav">
        <li><a class="header__nav-link">Link</a></li>
      </nav>
    </div>
  </div>
</header>
```

#### Footer
```html
<footer class="footer">
  <div class="container">
    <div class="footer__container">
      <img class="footer__logo" />
      <p class="footer__text">Texto</p>
    </div>
  </div>
</footer>
```

#### Card
```html
<div class="card">
  <div class="card__header">
    <h3 class="card__title">Título</h3>
  </div>
  <div class="card__body">Conteúdo</div>
  <div class="card__footer">
    <a class="btn btn--primary">Ação</a>
  </div>
</div>
```

#### Botão
```html
<!-- Variações de estilo -->
<a class="btn btn--primary">Primário</a>
<a class="btn btn--secondary">Secundário</a>
<a class="btn btn--success">Sucesso</a>

<!-- Variações de tamanho -->
<button class="btn btn--sm">Pequeno</button>
<button class="btn btn--lg">Grande</button>

<!-- Bloco completo -->
<button class="btn btn--block">Largura Total</button>
```

### 4. **Sistema de Grid e Layout**

#### Container
```html
<!-- Container padrão (max-width: 1200px) -->
<div class="container">Conteúdo</div>

<!-- Container pequeno -->
<div class="container container--sm">Conteúdo</div>

<!-- Sem limites -->
<div class="container container--full">Conteúdo</div>
```

#### Grid
```html
<!-- Grid 2 colunas (responsivo) -->
<div class="grid grid--2-cols">
  <div>Item 1</div>
  <div>Item 2</div>
</div>

<!-- Grid 3 colunas -->
<div class="grid grid--3-cols">
  <div>Item 1</div>
  <div>Item 2</div>
  <div>Item 3</div>
</div>
```

#### Seções
```html
<!-- Seção com padding padrão -->
<section class="section">Conteúdo</section>

<!-- Seção com padding grande -->
<section class="section section--lg">Conteúdo</section>
```

### 5. **Classes Utilitárias**

#### Tipografia
```html
<p class="text-center">Texto centralizado</p>
<p class="text-bold">Texto em negrito</p>
<p class="text-muted">Texto secundário</p>
<p class="text-primary">Texto em cor primária</p>
```

#### Cores
```html
<div class="bg-light">Fundo claro</div>
<div class="bg-primary">Fundo primário com texto branco</div>
```

#### Espaçamento
```html
<!-- Margin -->
<div class="m-md">Margin em todos os lados</div>
<div class="mt-lg">Margin-top maior</div>
<div class="mb-lg">Margin-bottom maior</div>

<!-- Padding -->
<div class="p-md">Padding</div>
<div class="px-md">Padding horizontal</div>
<div class="py-md">Padding vertical</div>
```

#### Bordas e Raio
```html
<div class="border rounded">Borda com raio</div>
<div class="border-top">Apenas borda superior</div>
<div class="rounded-lg">Raio maior</div>
```

#### Sombras
```html
<div class="shadow-sm">Sombra pequena</div>
<div class="shadow-md">Sombra média</div>
<div class="shadow-lg">Sombra grande</div>
```

---

## 🎨 Paleta de Cores

| Cor | Código | Uso |
|-----|--------|-----|
| **Primária** | `#333` | Texto principal |
| **Secundária** | `#777` | Texto secundário |
| **Accent** | `#2a5cdb` | Links, botões, destaques |
| **Sucesso** | `#27ae60` | Mensagens de sucesso |
| **Aviso** | `#f39c12` | Alertas |
| **Erro** | `#e74c3c` | Erros |
| **Fundo Claro** | `#f2eded` | Fundos de seções |
| **Fundo Muted** | `#f5f5f5` | Fundos secundários |

---

## 📱 Responsividade

O Design System é **mobile-first** com breakpoints:
- **Mobile**: < 768px
- **Tablet**: 768px - 1024px
- **Desktop**: > 1024px

```css
/* Ocultado em dispositivos móveis */
<div class="hide-mobile">Visível apenas em tablet/desktop</div>

/* Visível apenas em dispositivos móveis */
<div class="show-mobile">Visível apenas em mobile</div>
```

---

## ⚡ Transições

Velocidades predefinidas:
- **Rápido**: `--transition-fast` (150ms)
- **Normal**: `--transition-normal` (300ms)
- **Lento**: `--transition-slow` (500ms)

---

## 🚀 Como Usar

### 1. **Incluir CSS** (Ordem importante)
```html
<link rel="stylesheet" href="css/reset.css">
<link rel="stylesheet" href="css/tokens.css">
<link rel="stylesheet" href="css/base.css">
<link rel="stylesheet" href="css/layout.css">
<link rel="stylesheet" href="css/components.css">
<link rel="stylesheet" href="css/utils.css">
```

Ou usar o arquivo centralizado:
```html
<link rel="stylesheet" href="css/style.css">
```

### 2. **Criar Componente com BEM**
```html
<div class="card">
  <div class="card__header">
    <h3 class="card__title">Meu Card</h3>
  </div>
  <div class="card__body">
    <p>Conteúdo do card</p>
  </div>
</div>
```

### 3. **Usar Classes Utilitárias**
```html
<section class="section bg-light">
  <div class="container container--md">
    <h2 class="text-center mb-lg">Título</h2>
    <div class="grid grid--3-cols gap-md">
      <!-- Itens do grid -->
    </div>
  </div>
</section>
```

---

## ✨ Recursos Inclusos

✅ Design System completo com tokens  
✅ Componentes reutilizáveis (Header, Footer, Card, Botão, etc)  
✅ Sistema de Grid e Flexbox  
✅ Classes utilitárias completas  
✅ Responsividade mobile-first  
✅ Suporte a modo escuro (CSS Custom Properties)  
✅ Acessibilidade (a11y)  
✅ Transições e animações fluídas  
✅ Padrão BEM bem estruturado  
✅ Documentação completa  

---

## 🔧 Customização

Edite `tokens.css` para alterar:
- Cores (`:root` variables)
- Tipografia
- Espaçamento
- Bordas
- Sombras

Exemplo:
```css
:root {
  --color-primary: #000;      /* Muda a cor primária */
  --font-size-lg: 1.5rem;     /* Aumenta fontes grandes */
  --space-md: 20px;           /* Aumenta espaçamento */
}
```

---

## 📚 Arquivos e Responsabilidades

| Arquivo | Descrição |
|---------|-----------|
| `reset.css` | Remove estilos padrão do navegador |
| `tokens.css` | Define paleta de cores, tipografia, espaçamento |
| `base.css` | Estilos base para elementos HTML5 |
| `layout.css` | Container, grid, flexbox, seções |
| `components.css` | Componentes reutilizáveis (BEM) |
| `utils.css` | Classes auxiliares de estilo |
| `about.css` | Estilos específicos da página |
| `style.css` | Arquivo importador centralizado |

---

## 🎯 Melhores Práticas

1. **Use tokens**, não valores mágicos
2. **Siga o padrão BEM** para novas classes
3. **Mantenha HTML semântico**
4. **Use classes utilitárias** para pequenas alterações
5. **Respeite a escala de cores** definida
6. **Teste em diferentes dispositivos**
7. **Documente componentes customizados**

---

## 📞 Suporte

Para modificações ou novas funcionalidades, edite os arquivos CSS apropriados mantendo a estrutura modular do Design System.

---

**Refatoração concluída! ✨**
