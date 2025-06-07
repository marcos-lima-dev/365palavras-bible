# 📖 365Palavras Bible Data

> **Dados bíblicos estruturados em JSON para o app [365Palavras](https://github.com/marcos-lima-dev/365palavras)**

[![CDN](https://img.shields.io/badge/CDN-jsDelivr-orange)](https://cdn.jsdelivr.net/gh/marcos-lima-dev/365palavras-bible@main/)
[![License](https://img.shields.io/badge/License-Public%20Domain-green)](LICENSE)
[![Size](https://img.shields.io/github/repo-size/marcos-lima-dev/365palavras-bible)](https://github.com/marcos-lima-dev/365palavras-bible)

## 🎯 **Sobre**

Este repositório contém os **dados bíblicos em formato JSON** utilizados pelo aplicativo **365Palavras** - um tracker moderno para leitura bíblica anual.

### ✨ **Características:**
- 📚 **66 livros** da Bíblia completos
- 🔢 **3 traduções** disponíveis (ARA, ACF, NVI)
- ⚡ **Estrutura otimizada** para carregamento rápido
- 🌐 **CDN global** via jsDelivr
- 📱 **Mobile-first** design

## 📁 **Estrutura do Repositório**

```
📖 365palavras-bible/
├── 📂 ARA/          # Almeida Revista e Atualizada
│   ├── genesis.json
│   ├── exodo.json
│   ├── levitico.json
│   └── ... (66 livros)
├── 📂 ACF/          # Almeida Corrigida Fiel
│   ├── genesis.json
│   └── ... (66 livros)
├── 📂 NVI/          # Nova Versão Internacional
│   ├── genesis.json
│   └── ... (66 livros)
└── 📄 README.md
```

## 🚀 **Como Usar**

### **Via CDN (Recomendado)**
```javascript
// Carregar Gênesis em ARA
const response = await fetch('https://cdn.jsdelivr.net/gh/marcos-lima-dev/365palavras-bible@main/ARA/genesis.json')
const genesis = await response.json()
```

### **URLs Disponíveis:**
- **ARA:** `https://cdn.jsdelivr.net/gh/marcos-lima-dev/365palavras-bible@main/ARA/{livro}.json`
- **ACF:** `https://cdn.jsdelivr.net/gh/marcos-lima-dev/365palavras-bible@main/ACF/{livro}.json`
- **NVI:** `https://cdn.jsdelivr.net/gh/marcos-lima-dev/365palavras-bible@main/NVI/{livro}.json`

### **Livros Disponíveis:**
```
genesis, exodo, levitico, numeros, deuteronomio,
josue, juizes, rute, 1samuel, 2samuel, 1reis, 2reis,
1cronicas, 2cronicas, esdras, neemias, ester, jo,
salmos, proverbios, eclesiastes, cantares, isaias,
jeremias, lamentacoes, ezequiel, daniel, oseias,
joel, amos, obadias, jonas, miqueias, naum, habacuque,
sofonias, ageu, zacarias, malaquias, mateus, marcos,
lucas, joao, atos, romanos, 1corintios, 2corintios,
galatas, efesios, filipenses, colossenses,
1tessalonicenses, 2tessalonicenses, 1timoteo,
2timoteo, tito, filemom, hebreus, tiago, 1pedro,
2pedro, 1joao, 2joao, 3joao, judas, apocalipse
```

## 📊 **Estrutura dos Dados**

### **Estrutura ARA:**
```json
[
  {
    "abbrev": "gn",
    "book": "Gênesis",
    "chapters": [
      {
        "1": {
          "1": "No princípio criou Deus os céus e a terra.",
          "2": "A terra era sem forma e vazia..."
        }
      }
    ]
  }
]
```

### **Estrutura ACF/NVI:**
```json
[
  {
    "1": {
      "1": "No princípio criou Deus os céus e a terra.",
      "2": "A terra era sem forma e vazia..."
    }
  },
  {
    "2": {
      "1": "Assim foram acabados os céus e a terra..."
    }
  }
]
```

## ⚡ **Performance**

- 🚀 **CDN Global:** jsDelivr com cache automático
- 📦 **Tamanho médio:** ~100-500KB por livro
- ⚡ **Carregamento:** < 1 segundo via CDN
- 🔄 **Cache:** Automático no navegador

## 🛠️ **Integração com 365Palavras**

```javascript
// Exemplo de uso no app 365Palavras
import { loadBibleBook } from './bibleMapping'

const genesis = await loadBibleBook('genesis', 'ARA')
console.log(genesis.chapters[0]['1']['1']) // "No princípio..."
```

## 📱 **Aplicação Principal**

Este repositório é parte do **[365Palavras](https://github.com/marcos-lima-dev/365palavras)** - um aplicativo web progressivo (PWA) para acompanhamento de leitura bíblica anual.

### **Recursos do App:**
- 📅 **Plano de 365 dias** de leitura
- ✅ **Tracker de progresso** interativo  
- 📖 **Leitura integrada** com 3 traduções
- 🏆 **Sistema de conquistas**
- 📱 **PWA completo** para mobile

## 🤝 **Contribuições**

Contribuições são bem-vindas! Se encontrar algum erro nos textos ou quiser adicionar novas traduções:

1. **Fork** este repositório
2. **Crie uma branch** para sua feature
3. **Commit** suas mudanças
4. **Abra um Pull Request**

## 📄 **Licença**

Este projeto está sob **Domínio Público**. Os textos bíblicos são de domínio público e podem ser usados livremente.

## 🙏 **Créditos**

- **Textos bíblicos:** Baseados no repositório [BibliaJSON](https://github.com/wesleycsj/BibliaJSON)
- **Desenvolvido por:** [Marcos Lima](https://github.com/marcos-lima-dev)
- **Aplicação:** [365Palavras](https://365palavras.netlify.app)

---

<div align="center">

**⭐ Se este repositório foi útil, dê uma estrela! ⭐**

[🔗 Visite o App 365Palavras](https://365palavras.netlify.app) • [📱 Baixe como PWA](https://365palavras.netlify.app)

</div>