# Atividades de Manutenção e Alterações em Layout CSS

## 🎯 **Objetivo das Atividades**

Simular situações reais de trabalho onde os alunos precisam modificar códigos existentes, implementar melhorias e corrigir problemas em layouts.

---

## 📋 **ATIVIDADE 1: MUDANÇA DE IDENTIDADE VISUAL**

### **Cenário:**

O cliente da TechSolutions decidiu mudar a identidade visual da empresa. Você precisa atualizar o site com as novas cores e estilo.

### **Especificações da Nova Identidade:**

- **Cor primária:** #8e44ad (roxo)
- **Cor secundária:** #3498db (azul - manter)
- **Cor de destaque:** #f39c12 (laranja)
- **Estilo:** Mais moderno e arrojado

### **Tarefas a Executar:**

### **1.1 Alterações no Header (10 minutos)**

**O que fazer:**
- Mudar cor de fundo do header para a nova cor primária (#8e44ad)
- Alterar cor do logo para branco
- Mudar cor de hover dos links do menu para a cor de destaque (#f39c12)

**Código a modificar:**

```css
/* Encontrar e alterar estas regras no CSS */.header {
    background: #2c3e50; /* ALTERAR PARA #8e44ad */}
.logo h1 {
    color: #3498db; /* ALTERAR PARA white */}
.nav a:hover {
    color: #3498db; /* ALTERAR PARA #f39c12 */}
```

### **1.2 Alterações na Seção Hero (10 minutos)**

**O que fazer:**
- Mudar gradient do hero para usar as novas cores
- Alterar cor do botão para a cor de destaque
- Mudar cor de hover do botão para uma versão mais escura

**Código a modificar:**

```css
.hero {
    background: linear-gradient(135deg, #3498db, #2980b9);
    /* ALTERAR PARA: linear-gradient(135deg, #8e44ad, #9b59b6) */}
.btn-primary {
    background: #e74c3c; /* ALTERAR PARA #f39c12 */}
.btn-primary:hover {
    background: #c0392b; /* ALTERAR PARA #e67e22 */}
```

### **1.3 Alterações nos Cards de Serviço (5 minutos)**

**O que fazer:**
- Mudar cor do preço para a nova cor primária
- Alterar cor de hover dos cards

**Código a modificar:**

```css
.price {
    color: #e74c3c; /* ALTERAR PARA #8e44ad */}
.service-card:hover {
    /* Adicionar nova regra de hover com transform e box-shadow */}
```

### **Resultado Esperado:**

Site com nova identidade visual roxa/laranja, mantendo a funcionalidade e melhorando o visual.

---

## 📋 **ATIVIDADE 2: MELHORIAS DE RESPONSIVIDADE**

### **Cenário:**

O site do blog está com problemas de visualização em tablets. O cliente relatou que o layout não fica bom em telas médias (768px - 1024px).

### **Problemas Identificados:**

1. Sidebar muito estreita em tablets
2. Posts muito largos em telas médias
3. Menu de navegação quebra mal
4. Imagens não se adaptam bem

### **Tarefas a Executar:**

### **2.1 Corrigir Layout em Tablets (15 minutos)**

**O que fazer:**
- Criar media query específica para tablets (768px - 1024px)
- Ajustar proporção entre posts e sidebar
- Melhorar espaçamento

**Código a adicionar:**

```css
/* Adicionar nova media query entre as existentes */@media (min-width: 768px) and (max-width: 1024px) {
    .content-wrapper {
        gap: 2rem; /* Reduzir gap */    }
    .posts {
        flex: 1.5; /* Ajustar proporção */    }
    .sidebar {
        flex: 1; /* Ajustar proporção */    }
    .post-title {
        font-size: 1.6rem; /* Reduzir tamanho */    }
    .author-info {
        flex-direction: column; /* Empilhar em tablets */        text-align: center;    }
}
```

### **2.2 Melhorar Navegação Mobile (10 minutos)**

**O que fazer:**
- Criar menu hambúrguer para mobile
- Melhorar espaçamento dos links
- Adicionar transições suaves

**Código a modificar:**

```css
@media (max-width: 768px) {
    .nav {
        flex-direction: column; /* ALTERAR */        gap: 0.5rem; /* REDUZIR */        padding: 1rem; /* ADICIONAR */    }
    .nav a {
        padding: 0.8rem 1rem; /* ADICIONAR */        border-radius: 5px; /* ADICIONAR */        transition: all 0.3s ease; /* ADICIONAR */    }
    .nav a:hover {
        background: rgba(52, 152, 219, 0.1); /* ADICIONAR */    }
}
```

### **Resultado Esperado:**

Layout que funciona perfeitamente em todas as telas, especialmente tablets.

---

## 📋 **ATIVIDADE 3: OTIMIZAÇÃO DE PERFORMANCE VISUAL**

### **Cenário:**

A loja online está carregando lentamente e o cliente quer melhorar a experiência do usuário com animações e transições mais suaves.

### **Tarefas a Executar:**

### **3.1 Adicionar Animações de Loading (15 minutos)**

**O que fazer:**
- Criar animação de fade-in para os produtos
- Adicionar efeito de hover mais suave nos cards
- Implementar loading skeleton

**Código a adicionar:**

```css
/* Adicionar animações de entrada */@keyframes fadeInUp {
    from {
        opacity: 0;        transform: translateY(30px);    }
    to {
        opacity: 1;        transform: translateY(0);    }
}
.product-card {
    animation: fadeInUp 0.6s ease-out;    /* Adicionar delays diferentes para cada card */}
.product-card:nth-child(1) { animation-delay: 0.1s; }
.product-card:nth-child(2) { animation-delay: 0.2s; }
.product-card:nth-child(3) { animation-delay: 0.3s; }
.product-card:nth-child(4) { animation-delay: 0.4s; }
.product-card:nth-child(5) { animation-delay: 0.5s; }
.product-card:nth-child(6) { animation-delay: 0.6s; }
```

### **3.2 Melhorar Interações (10 minutos)**

**O que fazer:**
- Adicionar efeito de scale no hover das categorias
- Melhorar transição do botão de adicionar ao carrinho
- Criar efeito de pulse no ícone do carrinho

**Código a modificar e adicionar:**

```css
.category-card:hover {
    transform: translateY(-3px) scale(1.02); /* MODIFICAR */    box-shadow: 0 8px 16px rgba(0, 0, 0, 0.15); /* ADICIONAR */}
.btn-add-cart {
    transition: all 0.3s ease; /* MODIFICAR */}
.btn-add-cart:hover {
    background: #c0392b;    transform: translateY(-2px); /* ADICIONAR */    box-shadow: 0 4px 8px rgba(192, 57, 43, 0.3); /* ADICIONAR */}
/* Animação do carrinho */@keyframes pulse {
    0%, 100% { transform: scale(1); }
    50% { transform: scale(1.1); }
}
.cart:hover .cart-icon {
    animation: pulse 0.6s ease-in-out; /* ADICIONAR */}
```

### **Resultado Esperado:**

Site mais dinâmico e profissional com animações suaves que melhoram a experiência do usuário.
