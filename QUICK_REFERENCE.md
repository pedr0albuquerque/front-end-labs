# 📘 Guia Rápido - Componentes & Padrões

## 📍 Estrutura Básica de Página

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  
  <!-- Design System -->
  <link rel="stylesheet" href="css/reset.css">
  <link rel="stylesheet" href="css/tokens.css">
  <link rel="stylesheet" href="css/base.css">
  <link rel="stylesheet" href="css/layout.css">
  <link rel="stylesheet" href="css/components.css">
  <link rel="stylesheet" href="css/utils.css">
  
  <!-- Fontes -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="..." rel="stylesheet">
  
  <title>Página</title>
</head>

<body>
  <!-- Header -->
  <header class="header">...</header>
  
  <!-- Main Content -->
  <main>
    <section class="section">...</section>
  </main>
  
  <!-- Footer -->
  <footer class="footer">...</footer>
</body>
</html>
```

---

## 🧩 Componentes Prontos

### 1️⃣ Header com Navegação
```html
<header class="header">
  <div class="container">
    <div class="header__container">
      <img src="logo.png" alt="Logo" class="header__logo">
      <nav class="header__nav">
        <li><a href="#" class="header__nav-link header__nav-link--active">Ativo</a></li>
        <li><a href="#" class="header__nav-link">Link</a></li>
      </nav>
      <button class="header__toggle" aria-label="Menu">
        <span class="header__toggle-bar"></span>
        <span class="header__toggle-bar"></span>
        <span class="header__toggle-bar"></span>
      </button>
    </div>
  </div>
</header>

<script>
  document.querySelector('.header__toggle').addEventListener('click', function() {
    document.querySelector('.header__nav').classList.toggle('header__nav--open');
  });
</script>
```

### 2️⃣ Section com Container
```html
<section class="section section--lg">
  <div class="container">
    <h2>Título</h2>
    <p>Conteúdo aqui</p>
  </div>
</section>
```

### 3️⃣ Grid de Cards
```html
<div class="grid grid--3-cols">
  <div class="card">
    <div class="card__header">
      <h3 class="card__title">Título</h3>
    </div>
    <div class="card__body">
      <p>Descrição do card</p>
    </div>
    <div class="card__footer">
      <a href="#" class="btn btn--primary">Ação</a>
    </div>
  </div>
  <!-- Mais cards -->
</div>
```

### 4️⃣ Botões
```html
<!-- Primário -->
<a href="#" class="btn btn--primary">Primário</a>

<!-- Secundário -->
<button class="btn btn--secondary">Secundário</button>

<!-- Sucesso -->
<button class="btn btn--success">Sucesso</button>

<!-- Tamanhos -->
<button class="btn btn--sm">Pequeno</button>
<button class="btn btn--lg">Grande</button>

<!-- Bloco -->
<button class="btn btn--primary btn--block">Largura Completa</button>
```

### 5️⃣ Alertas
```html
<!-- Sucesso -->
<div class="alert alert--success">
  ✓ Operação realizada com sucesso!
</div>

<!-- Aviso -->
<div class="alert alert--warning">
  ⚠ Algo pode estar errado
</div>

<!-- Erro -->
<div class="alert alert--error">
  ✗ Erro ao processar
</div>

<!-- Info -->
<div class="alert alert--info">
  ℹ Informação importante
</div>
```

### 6️⃣ Badges
```html
<span class="badge">Padrão</span>
<span class="badge badge--primary">Primário</span>
<span class="badge badge--success">Sucesso</span>
<span class="badge badge--warning">Aviso</span>
<span class="badge badge--error">Erro</span>
```

### 7️⃣ Figuras/Imagens
```html
<figure class="figure">
  <img src="imagem.jpg" alt="Descrição" class="figure__img">
  <figcaption class="figure__caption">Legenda da imagem</figcaption>
</figure>
```

### 8️⃣ Breadcrumb
```html
<nav>
  <ol class="breadcrumb">
    <li class="breadcrumb__item"><a href="/" class="breadcrumb__link">Home</a></li>
    <li class="breadcrumb__item"><a href="/blog" class="breadcrumb__link">Blog</a></li>
    <li class="breadcrumb__item">Artigo Atual</li>
  </ol>
</nav>
```

### 9️⃣ Footer
```html
<footer class="footer">
  <div class="container">
    <div class="footer__container">
      <img src="logo.png" alt="Logo" class="footer__logo">
      <p class="footer__text">&copy; 2024. Todos os direitos reservados.</p>
    </div>
  </div>
</footer>
```

### 🔟 Flexbox Utilities
```html
<!-- Centro -->
<div class="flex flex--center">Centralizado</div>

<!-- Espaço entre -->
<div class="flex flex--between">Espaço entre</div>

<!-- Coluna -->
<div class="flex flex--column">
  <div>Item 1</div>
  <div>Item 2</div>
</div>

<!-- Com gap -->
<div class="flex flex--gap-lg">
  <div>Item 1</div>
  <div>Item 2</div>
</div>
```

---

## 🎨 Classes Utilitárias Comuns

### Tipografia
```html
<h1 class="text-center">Centralizado</h1>
<p class="text-bold">Negrito</p>
<span class="text-muted">Secundário</span>
<a class="text-primary">Destaque</a>
<small class="text-uppercase">MAIÚSCULA</small>
```

### Espaçamento
```html
<div class="mt-lg">Margin-top grande</div>
<div class="mb-lg">Margin-bottom grande</div>
<div class="p-lg">Padding tudo</div>
<div class="px-md px-horizontal">Padding horizontal</div>
<div class="py-md">Padding vertical</div>
<div class="m-0">Sem margin</div>
```

### Cores
```html
<div class="bg-light">Fundo claro</div>
<div class="bg-primary">Fundo primário</div>
<div class="bg-success">Fundo sucesso</div>
<p class="text-primary">Texto colorido</p>
<p class="text-muted">Texto secundário</p>
```

### Bordas
```html
<div class="border">Borda completa</div>
<div class="border-top">Apenas topo</div>
<div class="rounded">Raio padrão</div>
<div class="rounded-lg">Raio maior</div>
<div class="rounded-full">Totalmente redondo</div>
```

### Sombras
```html
<div class="shadow-sm">Sombra pequena</div>
<div class="shadow-md">Sombra média</div>
<div class="shadow-lg">Sombra grande</div>
```

---

## 🔄 Grid System

### 2 Colunas (Responsivo)
```html
<div class="grid grid--2-cols">
  <div>Item 1</div>
  <div>Item 2</div>
</div>

<!-- Em mobile vira 1 coluna automaticamente -->
```

### 3 Colunas
```html
<div class="grid grid--3-cols">
  <div>Item 1</div>
  <div>Item 2</div>
  <div>Item 3</div>
</div>
```

### 4 Colunas
```html
<div class="grid grid--4-cols">
  <!-- 4 itens -->
</div>
```

---

## 📱 Responsividade

### Mostrar/Ocultar por Device
```html
<!-- Apenas em mobile -->
<div class="show-mobile">Texto mobile</div>

<!-- Apenas em tablet/desktop -->
<div class="hide-mobile">Texto desktop</div>

<!-- Apenas em tablet -->
<div class="show-tablet hide-mobile">Tablet only</div>
```

---

## 🎯 Padrão BEM Explicado

```html
<!-- BLOCO: Component independente -->
<div class="card">
  
  <!-- ELEMENTO: Parte do bloco, não funciona sozinho -->
  <div class="card__header">
    <h3 class="card__title">Título</h3>
  </div>
  
  <!-- ELEMENTO modificado -->
  <div class="card__body card__body--highlight">
    Conteúdo especial
  </div>
  
</div>
```

### Regras BEM:
- **Bloco**: `.card` (componente independente)
- **Elemento**: `.card__item` (conectado ao bloco)
- **Modificador**: `.card--large` (variação)

---

## 💡 Exemplos de Páginas Completas

### Landing Page
```html
<header class="header">...</header>

<main>
  <!-- Hero Section -->
  <section class="section section--lg bg-primary">
    <div class="container text-center">
      <h1>Bem-vindo</h1>
      <p>Descrição</p>
      <a href="#" class="btn btn--primary btn--lg">CTA</a>
    </div>
  </section>

  <!-- Grid de Features -->
  <section class="section">
    <div class="container">
      <h2 class="text-center mb-lg">Características</h2>
      <div class="grid grid--3-cols">
        <div class="card">...</div>
        <div class="card">...</div>
        <div class="card">...</div>
      </div>
    </div>
  </section>
</main>

<footer class="footer">...</footer>
```

---

## ✅ Checklist para Nova Página

- [ ] Importar todos os CSS na ordem correta
- [ ] Usar `<header class="header">` para navegação
- [ ] Usar `<main>` para conteúdo principal
- [ ] Usar `<section class="section">` para seções
- [ ] Usar `<div class="container">` para limitar largura
- [ ] Usar `<footer class="footer">` para rodapé
- [ ] Aplicar `grid--*-cols` para layouts
- [ ] Usar `btn` para botões
- [ ] Usar `card` para conteúdo em cards
- [ ] Usar classes utilitárias (`text-center`, `mt-lg`, etc)
- [ ] Testar responsividade mobile/tablet/desktop

---

**Consulte `DESIGN_SYSTEM.md` para documentação completa!** 📚
