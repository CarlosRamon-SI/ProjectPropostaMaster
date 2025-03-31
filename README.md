# Planejamento - PropostaMaster

## Fase Inicial: Análise e Planejamento

### 1.1. Análise de Requisitos

**O que fazer:**  
Identifique os requisitos funcionais (o que o sistema deve fazer) e não funcionais (ex.: desempenho, usabilidade).  
Escreva um documento simples com:

#### Requisitos Funcionais (RF)
- [ ] **RF01:** O sistema deve ser web
- [ ] **RF02:** O frontend deve se comunicar via API com o backend
- [ ] **RF03:** O sistema deve cadastrar clientes com nome e email
- [ ] **RF04:** O sistema deve criar propostas com cliente
- [ ] **RF05:** O sistema deve criar produtos (Macro)
- [ ] **RF06:** O sistema deve inserir produtos(Macro e Micro) em proposta
- [ ] **RF07:** O sistema deve atualizar propostas
- [ ] **RF08:** O sistema deve atualizar produtos (Macro e Micro)
- [ ] **RF09:** O sistema deve listar todas as propostas cadastradas
- [ ] **RF10:** Propostas devem possuir:
    - Titulo da Proposta
    - Valor PTAX
    - Data PTAX
    - Data de Validade
- [ ] **RF11:** Produtos devem possuir:
    - Nome/Descrição
    - Moeda
    - Quantidade
    - Custo
    - Margem Percentual de Venda
    - Valor de Margem de Venda
    - Valor Unitário
    - Valor Total
    - Valor de Desconto
    - Valor Total c/ Desconto
    - Produtos Micro (Subprodutos/Componentes)
- [ ] **RF12:** O sistema deve integrar CRM via API Rest:
    - CRM Ploomes (Negócios, Produtos, Propostas, Empresas e Pessoas)
#### Requisitos Não Funcionais (RNF)
- [ ] **RNF01:** Propostas devem possuir:
    - Status da Proposta
    - Switch Resumos
    - Switch Bitdefender
    - Aliquota Anexo III Corrigida
    - Informações Importantes (Complementar)
- [ ] **RNF02:** Produtos devem possuir:
    - Categoria (Intermediação, Revenda, Único, Mensal ou Contrato)
    - Tipo (Produto ou Serviço)
    - Descrição adicional
    - Especificações Técnicas/Detalhes
    - Moeda Exibição
      - Switch Conversão
    - Switch Imposto
      - Aliquota de Imposto
      - Valor Total c/ Imposto
    - Switch Comissões
      - Taxa de Comissão
      - Valor de Comissão
      - Comissionado
    - Valor de Margem Estimada
    - Valor de Margem Espelho

    
    




**Dica:** Pesquise sobre requisitos funcionais e não funcionais. Use uma tabela ou lista numerada para organização.  
**Resultado:** Um documento claro que define o escopo técnico do "Proposta Fácil".

### 1.2. Estudo de Caso

**O que fazer:**  
Imagine um cenário real para justificar o sistema. Exemplo:

> "Uma pequena empresa de consultoria precisa gerenciar propostas comerciais para seus clientes. Atualmente, eles usam planilhas, o que é demorado e propenso a erros. O 'Proposta Fácil' será uma solução web para agilizar esse processo."

**Descreva:**
- **Contexto:** Quem usa, por que precisam.
- **Problema atual:** Ex.: falta de automação.
- **Solução proposta:** O sistema.

**Dica:** Veja exemplos de estudos de caso em engenharia de software para se inspirar.  
**Resultado:** Um texto curto (1-2 parágrafos) que dá propósito ao projeto.

### 1.3. Diagrama de Casos de Uso

**O que fazer:**  
Desenhe um diagrama básico mostrando os atores (ex.: "Usuário") e as ações (ex.: "Cadastrar Cliente", "Criar Proposta", "Listar Propostas").

- Use uma ferramenta como Draw.io, Lucidchart ou até papel e caneta.
- **Dica:** Pesquise sobre diagramas de casos de uso na UML (Unified Modeling Language).

**Resultado:** Uma visão visual de como o usuário interage com o sistema.

---

## 2. Design da Solução

### 2.1. Arquitetura do Sistema

**O que fazer:**  
Defina como o sistema será estruturado:

- **Back-end:** API REST com Node.js, TypeScript e POO, usando Express. Dados armazenados em memória (array) por enquanto.
- **Front-end:** Interface web com Vue.js e TypeScript, consumindo a API via HTTP.
- **Comunicação:** Requisições HTTP (GET, POST) entre front e back.

- Desenhe um diagrama simples mostrando: **Cliente (navegador) → Front-end → Back-end**.
- **Dica:** Estude o conceito de arquitetura cliente-servidor e camadas (ex.: MVC - Model, View, Controller).

**Resultado:** Um esboço da arquitetura para guiar o desenvolvimento.

### 2.2. Modelagem de Dados

**O que fazer:**  
Planeje as entidades com POO:

- **Cliente:** `id`, `nome`, `email`.
- **ItemProposta:** `descrição`, `preço`.
- **Proposta:** `id`, `cliente`, `itens (array)`, `data`, `valorTotal`.

Pense em como elas se relacionam (ex.: uma proposta tem um cliente e vários itens).

- **Dica:** Veja exemplos de diagramas de classes UML ou apenas liste os atributos e métodos.

**Resultado:** Uma estrutura clara para suas classes no back-end.

---

## 3. Gestão de Projetos com Sprints

Com a análise e o design prontos, usaremos o **Scrum** para executar o desenvolvimento, ajustando os sprints para refletir essa preparação.

### **Sprint 0: Preparação (Engenharia de Software)**
- **Duração:** 5-7 dias (ex.: 28/03/2025 a 03/04/2025).
- **Objetivo:** Definir requisitos e planejar o sistema.
- **Tarefas:**
  - Escrever os requisitos funcionais e não funcionais.
  - Criar o estudo de caso.
  - Desenhar o diagrama de casos de uso.
  - Planejar a arquitetura e modelagem de dados.
- **Critério de conclusão:** Documentos e diagramas prontos para guiar os próximos passos.

### **Sprint 1: Base do Back-end**
- **Duração:** 7 dias (ex.: 04/04/2025 a 10/04/2025).
- **Objetivo:** Configurar e criar a estrutura inicial do back-end.
- **Tarefas:**
  - Configurar Node.js e TypeScript.
  - Criar classes baseadas na modelagem (**Cliente, Proposta**).
  - Configurar uma rota simples no Express.
- **Critério de conclusão:** API rodando com uma resposta básica.

### **Sprint 2: API Completa**
- **Duração:** 7 dias (ex.: 11/04/2025 a 17/04/2025).
- **Objetivo:** Implementar as funcionalidades principais do back-end.
- **Tarefas:** (como no plano anterior, mas alinhadas aos requisitos).

### **Sprint 3: Front-end Básico**
- **Duração:** 7 dias (ex.: 18/04/2025 a 24/04/2025).
- **Objetivo:** Configurar e criar a interface inicial.

### **Sprint 4: Integração**
- **Duração:** 7 dias (ex.: 25/04/2025 a 01/05/2025).
- **Objetivo:** Conectar front-end e back-end.
