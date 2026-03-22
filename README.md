# 🚀 CI Demo Python

Projeto desenvolvido para demonstrar a implementação de um pipeline de **Integração Contínua (CI)** utilizando o GitHub Actions.

---

## 📌 Objetivo

Este projeto tem como objetivo aplicar, na prática, conceitos de Integração Contínua, garantindo que alterações no código sejam automaticamente validadas por meio de testes e análise estática.

---

## 🛠️ Tecnologias utilizadas

* Python 3.11
* Pytest (testes automatizados)
* Flake8 (análise estática de código)
* GitHub Actions (pipeline CI)

---

## ⚙️ Como executar o projeto localmente

### 1. Clonar o repositório

```bash
git clone https://github.com/raphagama/ci-demo-python
cd ci-demo-python
```

---

### 2. Criar ambiente virtual

```bash
python3 -m venv venv
source venv/bin/activate
```

---

### 3. Instalar dependências

```bash
pip install -r requirements.txt
```

---

### 4. Executar testes

```bash
pytest
```

---

### 5. Executar linter

```bash
flake8 .
```

---

## 🔄 Pipeline de Integração Contínua

O pipeline foi configurado utilizando o GitHub Actions e é executado automaticamente nos seguintes eventos:

* Push para a branch `main`
* Abertura de Pull Requests

### Etapas do pipeline:

1. Checkout do código
2. Configuração do ambiente Python
3. Instalação das dependências
4. Execução do Flake8 (lint)
5. Execução dos testes automatizados

---

## 🧠 Reflexão Técnica

### 🔹 Decisões técnicas adotadas

A escolha do GitHub Actions como ferramenta de Integração Contínua foi motivada pela sua integração nativa com o repositório, facilidade de configuração e ampla adoção no mercado. O pipeline foi estruturado de forma simples, porém eficiente, contemplando as etapas essenciais de validação de código.

A linguagem Python foi escolhida por sua simplicidade e rapidez de implementação, permitindo foco nos conceitos de CI. Para validação, foram utilizadas duas abordagens complementares: testes automatizados com Pytest e análise estática com Flake8.

Também foi adotado o uso de ambiente virtual para isolamento de dependências, garantindo reprodutibilidade do ambiente de desenvolvimento e compatibilidade com o pipeline.

---

### 🔹 Impactos da ausência de testes automatizados

A ausência de testes automatizados pode comprometer significativamente a qualidade do software, permitindo que erros sejam introduzidos sem detecção prévia. Isso aumenta o risco de falhas em produção e dificulta a manutenção do sistema.

Durante o desenvolvimento, ficou evidente que os testes automatizados atuam como um mecanismo de segurança, garantindo que alterações não quebrem funcionalidades existentes e promovendo maior confiança no processo de integração.

---

### 🔹 Possibilidades de evolução para Entrega Contínua

O pipeline atual pode ser evoluído para um modelo de Entrega Contínua (CD), incluindo etapas adicionais como:

* Deploy automatizado em ambiente de nuvem
* Utilização de containers com Docker
* Integração com ferramentas de monitoramento
* Execução de testes mais avançados (integração e carga)

Essas melhorias permitiriam automatizar todo o ciclo de vida da aplicação, desde o desenvolvimento até a entrega em produção.

---

### 🔹 Riscos técnicos mitigados pela Integração Contínua

A adoção de CI contribui para a mitigação de diversos riscos, como:

* Integração de código com erros
* Falta de padronização no desenvolvimento
* Problemas não detectados antes da entrega
* Inconsistências entre ambientes

Além disso, a execução automática em Pull Requests promove maior controle e qualidade nas alterações realizadas.

---

### 🔹 Considerações sobre o uso de linters

Foi necessário configurar o Flake8 para ignorar diretórios como o ambiente virtual (`venv`), evitando a análise de dependências externas. Essa prática garante que o linter foque exclusivamente no código do projeto, tornando a análise mais eficiente e relevante.

---

### 🔹 Considerações finais

Durante a implementação, foram observados avisos relacionados à evolução do ambiente de execução do GitHub Actions, como a descontinuação de versões do Node.js utilizadas internamente pelas actions. Esse aspecto evidencia que pipelines de CI exigem manutenção contínua e atualização tecnológica.

De forma geral, a experiência prática permitiu compreender a importância da automação no desenvolvimento de software, contribuindo para a melhoria da qualidade, confiabilidade e eficiência do processo de entrega.

---
