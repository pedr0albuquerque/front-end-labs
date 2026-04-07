# 🚀 Índice do Projeto - Front-End Labs

Bem-vindo ao projeto refatorado! Este é um guia rápido para navegar pelos arquivos e documentação.

## 📂 Estrutura do Projeto

```
front-end-labs/
├── 📄 index.html              ← Página inicial (Home)
├── 📄 about.html              ← Página sobre (Sobre Nós)
├── 📄 classes.html            ← Página de aulas/cursos
│
├── 📂 css/                    ← Arquivos de estilo
│   ├── reset.css              ← Reset CSS normalizado
│   ├── tokens.css             ← Variáveis globais do Design System
│   ├── base.css               ← Estilos base HTML5
│   ├── layout.css             ← Grid, containers, espaçamento
│   ├── components.css         ← Componentes reutilizáveis (BEM)
│   ├── utils.css              ← Classes utilitárias
│   ├── about.css              ← Estilos específicos da página about
│   └── style.css              ← Arquivo importador centralizado
│
├── 📂 img/                    ← Imagens do projeto
│
├── 📘 DESIGN_SYSTEM.md        ← Documentação completa do sistema
├── 📘 QUICK_REFERENCE.md      ← Guia rápido de componentes
├── 📘 INDEX.md                ← Este arquivo
└── 📘 README.md               ← Descrição original do projeto
```

---

## 🎯 Comece Aqui

### 1. **Entender a Estrutura**
👉 Leia [DESIGN_SYSTEM.md](DESIGN_SYSTEM.md) para uma visão completa do sistema

### 2. **Usar Componentes**
👉 Consulte [QUICK_REFERENCE.md](QUICK_REFERENCE.md) para exemplos rápidos

### 3. **Ver Páginas de Exemplo**
- [index.html](index.html) - Landing page com cards e CTA
- [about.html](about.html) - Página com conteúdo, grids e cards
- [classes.html](classes.html) - Página com grid de cursos

---

## 🎨 O Que Foi Refatorado

### ✅ Antes
- ❌ HTML desorganizado
- ❌ CSS sem padrão
- ❌ Sem componentes reutilizáveis
- ❌ Responsividade limitada
- ❌ Sem design system

### ✅ Depois
- ✅ HTML semântico e estruturado
- ✅ CSS modular e organizado
- ✅ Componentes reutilizáveis
- ✅ Mobile-first responsivo
- ✅ Design System completo

---

## 🧩 Componentes Principais

| Componente | Arquivo | Exemplo |
|------------|---------|---------|
| **Header** | components.css | Navegação com menu responsivo |
| **Footer** | components.css | Rodapé unificado |
| **Card** | components.css | Componente versátil para conteúdo |
| **Button** | components.css | 4 variações de estilo e 3 de tamanho |
| **Grid** | layout.css | 2, 3 ou 4 colunas (responsivo) |
| **Container** | layout.css | Largura máxima com padding |
| **Alert** | components.css | Alertas (sucesso, erro, aviso, info) |
| **Badge** | components.css | Rótulos coloridos |

---

## 🎯 Padrões Implementados

### 1. **Design Tokens** (Variáveis CSS)
Todas as decisões de design centralizadas em `tokens.css`:
- Cores
- Tipografia
- Espaçamento
- Sombras
- Transições

### 2. **BEM Naming Convention**
```
.bloco__elemento--modificador
```

Exemplos:
- `.header__container`
- `.footer__logo`
- `.btn--primary`
- `.card__header`

### 3. **Mobile-First Responsividade**
- **Mobile**: < 768px
- **Tablet**: 768px - 1024px
- **Desktop**: > 1024px

### 4. **Classes Utilitárias**
Combinação de classes para estilo rápido:
```html
<div class="text-center mt-lg mb-lg bg-light rounded">
  Texto centralizado com espaçamento e fundo
</div>
```

---

## 📋 Páginas Exemplo

### 🏠 Home (index.html)
- Section hero com CTA
- Grid de 3 cards com features
- Section com fundo colorido

### 📖 About (about.html)
- Seção intro com imagem
- Seção história com grid 2 colunas
- Grid 2x3 de cards com diferenciais
- Navegação responsiva

### 🎓 Classes (classes.html)
- Título e descrição
- Grid 3 colunas de cursos
- Cards com informações de nível
- CTA com botões múltiplos

---

## 🚀 Como Adicionar Novas Páginas

### 1. Criar arquivo HTML
```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  
  <!-- Importar Design System -->
  <link rel="stylesheet" href="css/reset.css">
  <link rel="stylesheet" href="css/tokens.css">
  <link rel="stylesheet" href="css/base.css">
  <link rel="stylesheet" href="css/layout.css">
  <link rel="stylesheet" href="css/components.css">
  <link rel="stylesheet" href="css/utils.css">
  
  <title>Minha Página</title>
</head>
<body>
  <header class="header">...</header>
  <main><!-- Conteúdo --></main>
  <footer class="footer">...</footer>
</body>
</html>
```

### 2. Usar componentes do design system
```html
<section class="section">
  <div class="container">
    <div class="grid grid--3-cols">
      <div class="card">
        <div class="card__body">Conteúdo</div>
      </div>
    </div>
  </div>
</section>
```

### 3. Combinar com classes utilitárias
```html
<h2 class="text-center mb-lg">Título</h2>
<p class="text-muted">Texto secundário</p>
```

---

## 🎨 Customização

### Alterar Cores
Edite `css/tokens.css`:
```css
:root {
  --color-primary: #seu-cor;
  --color-accent: #outra-cor;
}
```

### Alterar Tipografia
```css
:root {
  --font-family-primary: "Sua Fonte", sans-serif;
  --font-size-lg: 1.5rem;
}
```

### Alterar Espaçamento
```css
:root {
  --space-md: 18px;  /* Aumentar um pouco */
  --space-lg: 28px;
}
```

---

## 📚 Arquivos de Documentação

| Arquivo | Descrição |
|---------|-----------|
| [DESIGN_SYSTEM.md](DESIGN_SYSTEM.md) | Documentação completa com todos os componentes e padrões |
| [QUICK_REFERENCE.md](QUICK_REFERENCE.md) | Guia rápido com exemplos de código prontos para copiar |
| [INDEX.md](INDEX.md) | Este arquivo - visão geral do projeto |

---

## 💡 Dicas Importantes

### 1. **Sempre use os tokens**
```css
/* ❌ Evite valores mágicos -->
color: #333;

/* ✅ Use tokens -->
color: var(--color-text-primary);
```

### 2. **Combine classes reutilizáveis**
```html
<!-- ✅ Bom: Combina componentes -->
<button class="btn btn--primary btn--lg">Clique</button>

<!-- ❌ Evite: CSS adicional desnecessário -->
<button class="meu-botao-especial">Clique</button>
```

### 3. **Mantenha HTML semântico**
```html
<!-- ✅ Bom: Usa elementos corretos -->
<header><nav>...</nav></header>
<main>Conteúdo</main>
<footer>Rodapé</footer>

<!-- ❌ Evite: Div para tudo -->
<div class="header"><div class="nav">...</div></div>
```

### 4. **Mobile-first: teste em mobile primeiro**
```css
/* ✅ Bom: Começa com mobile -->
.card { width: 100%; }
@media (min-width: 768px) { .card { width: 50%; } }

/* ❌ Evite: Desktop first -->
.card { width: 50%; }
@media (max-width: 768px) { .card { width: 100%; } }
```

---

## 🔧 Troubleshooting

### Estilos não aplicam?
1. Verifique a ordem de import (reset → tokens → base → layout → components → utils)
2. Confirme que o arquivo CSS está no caminho correto
3. Limpe o cache do navegador (Ctrl+Shift+Del)

### Menu responsivo não funciona?
- Verifique se o JavaScript do hamburger está presente
- Teste em devtools (F12) modo mobile

### Grid não responsivo?
- Use classes `.grid--2-cols`, `.grid--3-cols`, etc
- Sistema responde automaticamente em mobile

---

## 📞 Próximos Passos

1. ✅ Explorar os componentes em [QUICK_REFERENCE.md](QUICK_REFERENCE.md)
2. ✅ Estudar o padrão BEM em [DESIGN_SYSTEM.md](DESIGN_SYSTEM.md)
3. ✅ Customizar tokens em `css/tokens.css`
4. ✅ Criar novas páginas reutilizando componentes
5. ✅ Adicionar estilos específicos em arquivos CSS separados

---

**🎉 Projeto refatorado com sucesso!**

Para qualquer dúvida sobre componentes ou padrões, consulte os arquivos de documentação acima.
