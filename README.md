# 📊 CSV Analyzer

Uma aplicação web para **importar, visualizar, filtrar e analisar arquivos CSV** diretamente no navegador.

O **CSV Analyzer** foi desenvolvido para facilitar a exploração de dados sem a necessidade de abrir ferramentas mais complexas. O usuário pode carregar um arquivo CSV e, em uma única interface, pesquisar informações, aplicar filtros, identificar os maiores e menores valores, visualizar estatísticas e exportar os dados resultantes.

> **Importe → Analise → Filtre → Explore → Exporte**

---

## ✨ Funcionalidades

### 📁 Importação de CSV

* Upload de arquivos `.csv`
* Suporte a **Drag and Drop**
* Detecção automática do separador quando possível
* Identificação automática do cabeçalho
* Exibição da quantidade de linhas e colunas
* Possibilidade de trocar o arquivo carregado

### 🔎 Pesquisa

* Pesquisa em todas as colunas
* Pesquisa por coluna específica
* Atualização dos resultados em tempo real

### 🔧 Filtros

Filtros adaptados ao tipo de cada coluna.

**Colunas numéricas**

* Maior que
* Menor que
* Igual a
* Maior ou igual a
* Menor ou igual a
* Menor ou igual a
* Entre dois valores

**Colunas de texto**

* Contém
* Não contém
* Igual a
* Começa com
* Termina com
* Seleção de valores específicos

**Colunas de data**

* Antes de
* Depois de
* Igual a
* Entre duas datas

### ↕️ Ordenação

Permite ordenar os dados de forma:

* Crescente
* Decrescente
* A → Z
* Z → A

Também é possível encontrar rapidamente os **maiores e menores valores** de uma coluna.

### 🏆 Top & Bottom

Crie análises rápidas utilizando:

* Top 5
* Top 10
* Top 20
* Bottom 5
* Bottom 10
* Bottom 20

Exemplo:

> Top 10 produtos por faturamento

### 📈 Estatísticas

Para colunas numéricas, o sistema pode calcular:

* Soma
* Média
* Mediana
* Maior valor
* Menor valor
* Quantidade de valores
* Quantidade de valores únicos

Também são identificados os **valores ausentes**.

### 📊 Gráficos

Quando aplicável, os dados podem ser visualizados através de:

* Gráficos de barras
* Gráficos de linhas
* Gráficos de distribuição

O usuário pode selecionar as colunas utilizadas para construir a visualização.

### 📤 Exportação

É possível exportar:

* Dados filtrados em um novo CSV
* Resultados da análise

### 🔄 Limpeza de filtros

O botão **Limpar filtros** permite restaurar rapidamente os dados originais e remover as condições aplicadas.

---

## 🖥️ Interface

A aplicação utiliza uma interface **clean, moderna e responsiva**, sem sidebar lateral.

O fluxo principal acontece em uma única página:

```text
┌───────────────────────────────────────────────┐
│                 CSV ANALYZER                  │
│      Analise, filtre e explore seus dados     │
└───────────────────────────────────────────────┘

              📁 Importar CSV

        Arquivo: vendas.csv
        Linhas: 2.540 | Colunas: 8

┌───────────────────────────────────────────────┐
│              Resumo dos dados                │
├──────────┬──────────┬───────────┬─────────────┤
│ Linhas   │ Colunas  │ Vazios    │ Maior valor │
└──────────┴──────────┴───────────┴─────────────┘

              🔎 Filtrar dados

        Pesquisa | Coluna | Condição | Valor

              📊 Tabela de dados

              📈 Análise

              📤 Exportar
```

O objetivo é manter todas as ferramentas importantes acessíveis sem transformar a aplicação em um dashboard excessivamente complexo.

---

## 🚀 Tecnologias

O projeto foi pensado para funcionar diretamente no navegador utilizando tecnologias web.

### Base

* HTML5
* CSS3
* JavaScript

### Possíveis bibliotecas

Dependendo da implementação, podem ser utilizadas bibliotecas específicas para:

* Processamento de CSV
* Manipulação de tabelas
* Criação de gráficos

A aplicação prioriza uma arquitetura simples e o processamento local dos dados.

---

## 🔐 Privacidade

O processamento dos arquivos é realizado **localmente no navegador**, evitando o envio desnecessário dos dados para servidores externos.

Isso significa que arquivos contendo informações sensíveis podem ser analisados sem precisar sair da máquina do usuário, desde que a implementação utilizada mantenha todo o processamento no cliente.

---

## 📋 Exemplo de uso

Imagine um arquivo:

```csv
Produto,Quantidade,Preco,Data
Notebook,10,3500,2026-01-10
Mouse,50,120,2026-01-11
Teclado,30,250,2026-01-12
Monitor,15,1800,2026-01-13
```

Após importar o arquivo, o usuário pode:

1. Ver todas as informações em uma tabela.
2. Encontrar o produto com o maior preço.
3. Encontrar o produto com a menor quantidade.
4. Filtrar produtos com preço acima de `R$ 500`.
5. Pesquisar por um produto específico.
6. Ordenar os preços do maior para o menor.
7. Visualizar estatísticas das colunas numéricas.
8. Exportar somente os registros filtrados.

---

## ⚙️ Como executar o projeto

### 1. Clone o repositório

```bash
git clone https://github.com/SEU-USUARIO/csv-analyzer.git
```

### 2. Entre na pasta

```bash
cd csv-analyzer
```

### 3. Execute o projeto

Caso seja uma aplicação web estática, basta abrir o arquivo:

```text
index.html
```

em um navegador.

Para uma experiência de desenvolvimento mais adequada, também pode ser utilizado um servidor local, como o **Live Server** do VS Code.

---

## 📂 Estrutura do projeto

Uma estrutura possível:

```text
csv-analyzer/
│
├── index.html
├── css/
│   └── style.css
│
├── js/
│   ├── app.js
│   ├── csv.js
│   ├── filters.js
│   ├── analysis.js
│   ├── table.js
│   └── export.js
│
├── assets/
│   └── icons/
│
├── README.md
└── .gitignore
```

### Principais responsabilidades

| Arquivo       | Responsabilidade                   |
| ------------- | ---------------------------------- |
| `index.html`  | Estrutura da aplicação             |
| `style.css`   | Estilos e responsividade           |
| `app.js`      | Inicialização e integração         |
| `csv.js`      | Importação e processamento do CSV  |
| `filters.js`  | Sistema de filtros                 |
| `analysis.js` | Estatísticas e análises            |
| `table.js`    | Renderização e ordenação da tabela |
| `export.js`   | Exportação dos resultados          |

---

## 📊 Tipos de análise

O CSV Analyzer pode trabalhar principalmente com três categorias de dados:

### 🔢 Numéricos

Exemplos:

```text
Preço
Quantidade
Faturamento
Idade
Nota
```

Permitem operações matemáticas e comparações.

### 🔤 Texto

Exemplos:

```text
Nome
Produto
Cidade
Categoria
Status
```

Permitem pesquisas e filtros textuais.

### 📅 Datas

Exemplos:

```text
2026-01-10
2026-05-20
2026-09-30
```

Permitem análises baseadas em períodos.

---

## 🎯 Objetivo do projeto

O projeto tem como objetivo criar uma ferramenta simples para **exploração e análise inicial de dados**, tornando operações comuns de análise acessíveis mesmo para usuários que não possuem experiência com ferramentas avançadas de Data Analytics.

Além da aplicação prática, o projeto também serve como estudo de:

* Manipulação de dados
* JavaScript
* Processamento de arquivos
* Estatística básica
* Desenvolvimento de interfaces
* Filtragem e transformação de dados
* Visualização de informações
* Performance no navegador

---

## 🔮 Melhorias futuras

Algumas funcionalidades que podem ser adicionadas posteriormente:

* Suporte a arquivos XLSX
* Mais tipos de gráficos
* Agrupamento de dados
* Tabelas dinâmicas
* Detecção mais avançada de tipos
* Tratamento de valores duplicados
* Análise de correlação
* Exportação em JSON
* Exportação em Excel
* Histórico de análises
* Temas claro e escuro
* Processamento de arquivos ainda maiores
* Virtualização avançada da tabela

---

## 🛠️ Status do projeto

**Em desenvolvimento 🚧**

O projeto está sendo desenvolvido e pode receber novas funcionalidades, melhorias de interface e otimizações de desempenho.

---

## 🤝 Contribuição

Contribuições, sugestões e melhorias são bem-vindas.

Para contribuir:

```bash
# Crie um fork do projeto

# Clone o seu fork
git clone https://github.com/SEU-USUARIO/csv-analyzer.git

# Crie uma branch
git checkout -b feature/nova-funcionalidade

# Faça suas alterações

# Commit
git commit -m "feat: adiciona nova funcionalidade"

# Push
git push origin feature/nova-funcionalidade
```

Depois, abra um **Pull Request**.

---

## 📄 Licença

Este projeto pode ser distribuído sob a licença **MIT**.

Consulte o arquivo `LICENSE` para mais informações.

---

## 👨‍💻 Autor

Desenvolvido por **Arthur Galvão**.

📌 GitHub: [ArthurGmartins2307](https://github.com/ArthurGmartins2307)

📌 LinkedIn: [arthurgalvaodev](https://www.linkedin.com/in/arthurgalvaodev/)

---

## ⭐ Apoie o projeto

Caso o projeto tenha sido útil ou interessante para você, considere deixar uma ⭐ no repositório.

**CSV Analyzer — transforme arquivos CSV em informações úteis.**

