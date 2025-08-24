# 🛒 Shopping Cart Bug Challenge

[![Deploy Status](https://github.com/willvitorino/shopping-cart-bug-1/actions/workflows/deploy.yml/badge.svg)](https://github.com/willvitorino/shopping-cart-bug-1/actions/workflows/deploy.yml)
[![Vue.js](https://img.shields.io/badge/Vue.js-3.x-4FC08D?style=flat&logo=vue.js)](https://vuejs.org/)
[![Vite](https://img.shields.io/badge/Vite-5.x-646CFF?style=flat&logo=vite)](https://vitejs.dev/)
[![TailwindCSS](https://img.shields.io/badge/Tailwind-3.x-06B6D4?style=flat&logo=tailwindcss)](https://tailwindcss.com/)

> **Dificuldade:** ⭐ (Iniciante)  
> **Capítulo:** Chapter 5: Challenge Roundup  
> **Tecnologia:** Vue.js 3  

## 📋 Descrição do Desafio

Este projeto é um **desafio de debugging** onde existem bugs escondidos em um Widget de Carrinho de Compras. Sua missão é encontrar e eliminar todos esses bugs para que a aplicação funcione corretamente!

## 🎯 Requisitos Funcionais

- [ ] **Atualização automática do total:** O preço total deve ser atualizado automaticamente quando a quantidade de qualquer item for alterada
- [ ] **Formatação de preços:** Todos os preços devem ser exibidos com 2 casas decimais (itens individuais e total)
- [ ] **Validação de quantidade:** Não deve ser possível inserir valores negativos para a quantidade

## 🔧 Stack Tecnológica

| Tecnologia | Versão | Descrição |
|------------|--------|-----------|
| **Vue.js** | 3.x | Framework JavaScript progressivo |
| **Vite** | 5.x | Build tool e dev server |
| **TailwindCSS** | 3.x | Framework CSS utility-first |
| **Vitest** | - | Framework de testes unitários |

## ⚠️ Considerações Importantes

> 🚨 **Atenção:** Não remova os atributos `data-test` presentes no código. Eles são utilizados para testes automatizados.

> 💡 **Dica:** O TailwindCSS está pré-configurado. Você pode utilizá-lo para estilização, mas não é obrigatório.

## 🎥 Exemplo da Aplicação Funcionando

Veja como a aplicação deve funcionar quando todos os bugs forem corrigidos:

![Exemplo da aplicação funcionando](https://i.imgur.com/0qSRdU0.gif)

## 🚀 Como Executar o Projeto

### Pré-requisitos
- Node.js 18+ 
- npm ou yarn

### Instalação e Execução

```bash
# Clone o repositório
git clone https://github.com/willvitorino/shopping-cart-bug-1.git

# Entre no diretório
cd shopping-cart-bug-1

# Instale as dependências
npm install
# ou
yarn install

# Execute o projeto em modo de desenvolvimento
npm run dev
# ou
yarn dev

# Execute os testes
npm run test
# ou
yarn test

# Build para produção
npm run build
# ou
yarn build
```

## 🌐 Deploy Automático - GitHub Pages

Este projeto está configurado para **deploy automático** no GitHub Pages através do GitHub Actions.

### 📋 Configuração do GitHub Pages

1. **Habilitar GitHub Pages:**
   - Acesse: `Settings` → `Pages` no repositório
   - Em **Source**, selecione `GitHub Actions`

2. **Deploy Automático:**
   - Cada push na branch `main` trigga o deploy automaticamente
   - Workflow configurado em `.github/workflows/deploy.yml`

3. **Deploy Manual (opcional):**
   ```bash
   npm install
   npm run deploy
   ```

### ⚙️ Configurações de Deploy

| Configuração | Valor |
|--------------|-------|
| **Base URL** | `/shopping-cart-bug-1/` |
| **Workflow** | GitHub Actions + Node.js 18 |
| **Pasta de Build** | `dist/` |
| **URL de Produção** | [https://willvitorino.github.io/shopping-cart-bug-1/](https://willvitorino.github.io/shopping-cart-bug-1/) |

## 📁 Estrutura do Projeto

```
shopping-cart-bug-1/
├── .github/
│   └── workflows/
│       └── deploy.yml          # Workflow de deploy
├── public/
│   └── favicon.ico
├── src/
│   ├── components/
│   │   ├── CartTotal.vue       # Componente do total do carrinho
│   │   ├── ProductItem.vue     # Componente de item do produto
│   │   └── ShoppingCart.vue    # Componente principal do carrinho
│   ├── App.vue                 # Componente raiz
│   └── main.js                 # Ponto de entrada
├── tests/
│   └── app.test.ts            # Testes automatizados
├── index.html                 # Template HTML
├── package.json               # Dependências e scripts
├── vite.config.mjs           # Configuração do Vite
├── tailwind.config.js        # Configuração do Tailwind
└── README.md                 # Este arquivo
```

## 🧪 Testando a Aplicação

```bash
# Executar testes unitários
npm run test

# Executar testes em modo watch
npm run test:watch

# Gerar relatório de cobertura
npm run test:coverage
```

## 🐛 Bugs Conhecidos para Corrigir

Este desafio contém bugs intencionais que você deve encontrar e corrigir. Analise cuidadosamente:

- ✅ Lógica de cálculo do total
- ✅ Formatação de números decimais
- ✅ Validação de entrada de dados
- ✅ Reatividade dos componentes Vue

## 🤝 Contribuindo

Este é um projeto educacional. Sinta-se à vontade para:

1. Fazer fork do projeto
2. Criar uma branch para sua feature (`git checkout -b feature/minha-feature`)
3. Commit suas mudanças (`git commit -m 'Adiciona minha feature'`)
4. Push para a branch (`git push origin feature/minha-feature`)
5. Abrir um Pull Request

## 📝 Licença

Este projeto é parte de um curso de treinamento e está disponível para fins educacionais.

---

**Desenvolvido com ❤️ para aprendizado de Vue.js e debugging**
